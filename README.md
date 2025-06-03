# Agent Practice
practice with AI agents in Python based on langchain and langgraph modules. 

The LLM model is 'gemini-2.0-flash'. To use it, you can setup an API key for the env variable 

GOOGLE_API_KEY

Files 'RAG_bsic.ipynb', 'RAG_chain.ipynb' and 'RAG_agent.ipynb' uses pgvector on a docker container. 
The connection used is

"postgresql+psycopg://langchain:langchain@localhost:6024/langchain"

So, you can run 

docker run --name langchain_pgvector \
  -e POSTGRES_USER=langchain \
  -e POSTGRES_PASSWORD=langchain \
  -e POSTGRES_DB=langchain \
  -p 6024:5432 \
  -d ankane/pgvector

form terminal or create and run a corresponding .yml file. Alternatively, you can create your own docker container, but remember to change the connection in the script!
