# MarketEnterpriseAgent_KaggleGoogleCourse

Throughout this repository's notebook you will find my Capstone Project related to the Google+ Kaggle 5-day Agents course. 

# 🚨 Problem to solve

There is a widespread problem within companies dedicated to trade with any kind of products, companies that typically act as intermediaries between suppliers and the end customer. 

The core of the business is focused on profiting from these transactions, constantly searching through different suppliers or competitors for different offers, buying when they believe they can sell at a price high enough to make a profit.

The problem arises from the **complexity of analyzing** every supplier or store that offers each product, making it tedious (and almost impossible) to cover all possible purchasing options for a given product. 

# ✅ Solution

Create an AI-based solution that addresses this issue. In a simple, effective, and natural way, this tool allows users to search for information on any product online, simplifying this task to an extreme degree.

- Each query automatically returns the best offer for each product, as well as relevant information such as delivery time, supplier, and product status. It also allows filtering by product status.

- It will also provide the user with information on the current price, indicating the price trend, its position relative to historical data, and even the highest and lowest prices reached by that supplier for that product.

- After obtaining this information, the user will also be given the option to quickly purchase the product, specifying the desired condition and quantity. By doing this, the user will obtain all relevant information to make a purchase.

With this workflow, **a complete comparison of suppliers, prices, and market flows can be performed for a single product, and a purchase order can be placed with the desired conditions, all in a matter of seconds.**

# ⚙️ Knowledge applied

During the agent's creation, several techniques and ideas learned during the course were applied. Among others:

- Various **custom tools** were used to simulate real-world scenarios. These scenarios would access APIs and search engines anywhere on the network. All agents created in the workflow and the tests previously mentioned were **powered by an LLM agent** (Gemini 2.5 Flash Lite in this case)

- These tools were used sequentially with **built-in functions** (they could also be independent models), resulting in a complete workflow for information retrieval and purchase management. Apart, in the last agent, a combination of an agent and another function (**sequential agents**) worked together as tools of the agent.

- The **agent's evaluation** was implemented using the ADK provided by Google, where another agent maintains a conversation and automates the various tests, making the process more efficient and replicable. The configuration of these tests was adapted for better results.

- A implementation of **long-running operations** was also added. By doing this, the risk of the agent performing actions that would be bad-formed or compromise any part of a company is drastically reduced, forcing the agent to have a confirmation before it acts.

# 🎯 Conclusion

Throughout this notebook, I presented an **AI agent-based solution that addresses a real need for many companies**, and is also applicable to end users. I simulated a real-world environment by creating databases and methods that simulate the use of an API or similar. By using real APIs and search engines. This solution could be integrated into real-world environments.

Having the real scenario simulated, a **first agent that handles analysis** over the products and obtains all information related to it was developed. Later, this **agent was improved by adding another tool**. This tool performs as a purchase manager, retrieving all information about the purchase options, simulating the operation.

After developing that agent, a solution focused on **advanced model evaluation** was presented, compared to the one shown in the course. By creating these evaluation tests, **another model performs the conversation on the user side**, having a full conversation with our agent. That allows any developer an easy way to debug and understand the process inside the agent reasoning.

Later, another clear improvement appeared. When the agent receives an order to place a big purchase order, it could be risky (for example, if the user commits an error in the input provided to the model). For that, **I added to the model long-running operations**. By doing this, a human approval will be required if the agent detects that an order is expensive (at least 1000$), **avoiding auto-placement of an expensive order without explicit confirmation**.

Related to next steps, ideas like looking for a type of product (instead of the product itself), looking for the best products of a specific vendor, or filtering directly the options that don't have a delivery fee could be well-fitted improvements.

As a summary, I applied a lot of the knowledge acquired during this short and intense course to a "simulated" real environment, having an agent that helps to avoid (or at least reduce) the commented problem, requesting human approval when a risky operation is taking place, and developing a useful evaluation process.
