# LLM_SQL_agent

Streamlit based frontend to chat with your SQL db, the llm agent can run queries to answer questions.

This is clone of this script from langchain repo,

https://github.com/langchain-ai/streamlit-agent/blob/main/streamlit_agent/chat_with_sql_db.py


# My Reviews


**Issues:**

1. **Terrible Results:** When testing the SQL agent with GPT 4 and Claude via aws bedrock, I found that the results were consistently terrible, even when using the default sample database.
2. **Poor Handling of Joins:** The SQL agent struggled to perform simple joins, which is a fundamental SQL operation. This limitation significantly hindered its usefulness.
3. **Looping Behavior:** I observed that when I asked the same question multiple times, the SQL agent often got stuck in a loop, providing repetitive or unhelpful responses.
4. **SQL Function Errors:** There seemed to be an underlying issue with the SQL function calls, as it occasionally added '/n' to table names, leading to query failures. This is a critical problem that needs addressing.
5. **Limited Schema Support:** The SQL agent appeared to work only with a single database schema. When attempting to connect it to a data warehouse with hundreds of schemas, it defaulted to the public schema. It was unable to comprehend the presence of multiple schemas and tables within the data warehouse.

**Suggestions:**

1. **Custom Debugging Tools:** To improve the overall performance and usability of this SQL agent, it would be worthwhile to invest time in developing custom debugging tools. These tools can help identify and resolve issues more efficiently.
2. **Continued Experimentation:** I plan to continue experimenting with the SQL agent to see if it can be made to work better, at least for handling simple queries. It's essential to explore potential improvements.

These issues and suggestions should provide a clear picture of the challenges I encountered while testing the SQL agent and my recommendations for addressing them. If you have any further questions or need additional details, please feel free to ask.
