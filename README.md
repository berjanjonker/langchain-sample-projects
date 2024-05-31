# LangChain Sample Projects  
   
Welcome to the LangChain Sample Projects repository! This repository contains four example projects demonstrating different capabilities of the LangChain library. Each project is presented in a Jupyter notebook and showcases various functionalities such as creating simple chains, using tools, querying CSV files, and interacting with SQL databases.
   
## Table of Contents  
   
1. [Project 1: Simple Sequential Chain](#project-1-simple-sequential-chain)  
2. [Project 2: Simple Tools](#project-2-simple-tools)  
3. [Project 3: CSV Manipulation](#project-3-csv-manipulation)  
4. [Project 4: SQL Database Interaction](#project-4-sql-database-interaction)  
   
## Project 1: Simple Sequential Chain  
   
**Notebook**: `langchain_simple_chain.ipynb`  
   
This project demonstrates how to create a simple sequential chain using LangChain. It involves two linked chains:  
1. **Genre Recommender**: Recommends related movie genres based on the user's favorite genre.  
2. **Movie Recommender**: Suggests movies based on the recommended genres.  
   
### Key Components:  
- **AzureChatOpenAI**: Utilizes Azure's OpenAI API for the language model.  
- **PromptTemplate**: Defines the prompts for the language model.  
- **SimpleSequentialChain**: Links the two chains together.  
   
**Example Output**:  
```plaintext
> Favorite movie genre: War
Output:
> Entering new SimpleSequentialChain chain...  
1. Historical Drama - "Braveheart"  
2. Action - "Saving Private Ryan"  
3. Thriller - "Zero Dark Thirty"  
> Finished chain.  
```  
   
## Project 2: Simple Tools  
   
**Notebook**: `langchain_simple_tools.ipynb`  
   
This project shows how to use pre-built tools in LangChain and create an agent that can respond to user questions using those tools.  
   
### Key Components:  
- **AzureChatOpenAI**: Utilizes Azure's OpenAI API for the language model.  
- **load_tools**: Loads tools like `llm-math` and `wikipedia`.
- **initialize_agent**: Creates an agent using the loaded tools.  
   
**Example Output**:  
```plaintext  
> Question: Add up the birth years of Einstein, Putin and Vincent van Gogh
> Entering new AgentExecutor chain...  
Final Answer: 5684  
> Finished chain.  
```  
   
## Project 3: CSV Manipulation  
   
**Notebook**: `langchain_csv.ipynb`  
   
This project demonstrates how to define custom tools for LangChain and chain them together to perform complex tasks involving CSV files and Wikipedia queries.  
   
### Key Components:  
- **AzureChatOpenAI**: Utilizes Azure's OpenAI API for the language model.  
- **tool**: Defines custom tools.  
- **initialize_agent**: Creates an agent using the custom tools.  
   
**Example Output**:  
```plaintext
> Question: Pick a random place from the Netherlands. Finds information about that place. And take a fun fact from that information and write a column about it.
> Entering new AgentExecutor chain...  
Final Answer: The flag of Langerak, a small town in the Netherlands, has been praised for its "unique historical significance". But let's be honest, it's just a flag based on one used in 1938 to celebrate the fortieth anniversary of Queen Wilhelmina's reign. It was never officially established and was only used during a parade in Amsterdam. Let's not forget that it also contains the city's coat of arms. So let's stop pretending this is some huge historical symbol. It's just a flag with a questionable connection to a royal event.
> Finished chain.  
```  
   
## Project 4: SQL Database Interaction  
   
**Notebook**: `langchain_sql.ipynb`  
   
This project demonstrates how to interact with an SQL database using LangChain. It involves querying a sample SQLite database and retrieving information.  
   
### Key Components:  
- **AzureChatOpenAI**: Utilizes Azure's OpenAI API for the language model.  
- **SQLDatabase**: Connects to an SQLite database.  
- **create_sql_agent**: Creates an agent for interacting with the SQL database.  
   
**Example Output**:  
```plaintext
> Question: List the total sales per country. Which country's customers spent the most?
> Entering new SQL Agent Executor chain...  
Final Answer: The country whose customers spent the most is the USA, with a total sales amount of $523.06.  
> Finished chain.  
```  
   
## Getting Started  
   
1. **Clone the repository**:  
    ```sh  
    git clone https://github.com/your-repo/langchain-sample-projects.git  
