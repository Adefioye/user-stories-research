# USER STORIES RESEARCH USING LLM EMBEDDINGS

# RESEARCH QUESTION 1
1. Install necessary packages for embedding user story
```
pip install ollama langchain langchain_community
ollama pull llama3
ollama pull phi3
ollama pull mistral 
```
2. Embeddings were performed using `Llama 3 8B`, `Mistral 7B` and `Phi-3 3.8B` parameter model
3. Install packages for storing embeddings, preprocessing
```
pip install nltk supabase
``` 
4. Database setup
```
-- Enable the pgvector extension
create extension vector;

CREATE TABLE "g12-camperplus" (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_story_id TEXT,
  story TEXT,
  llama_embedding vector,
  mistral_embedding vector,
  phi3_embedding vector
);
```


