# `Auto-evaluator` :brain: :memo:

> **Note**
> See the HuggingFace space for this app: https://huggingface.co/spaces/rlancemartin/auto-evaluator

> **Note**
> See the hosted app: https://autoevaluator.langchain.com/

> **Note**
> Code for the hosted app is also open source: https://github.com/langchain-ai/auto-evaluator

This is a lightweight evaluation tool for question-answering using Langchain to:

- Ask the user to input a set of documents of interest

- Apply an LLM (`GPT-3.5-turbo`) to auto-generate `question`-`answer` pairs from these docs

- Generate a question-answering chain with a specified set of UI-chosen configurations

- Use the chain to generate a response to each `question`

- Use an LLM (`GPT-3.5-turbo`) to score the response relative to the `answer`

- Explore scoring across various chain configurations

**Run as Streamlit app**

`pip install -r requirements.txt`

`streamlit run auto-evaluator.py`

**Inputs**

`num_eval_questions` - Number of questions to auto-generate (if the user does not supply an eval set)

`split_method` - Method for text splitting

`chunk_chars` - Chunk size for text splitting
 
`overlap` - Chunk overlap for text splitting
  
`embeddings` - Embedding method for chunks
 
`retriever_type` - Chunk retrieval method

`num_neighbors` - Neighbors for retrieval 

`model` - LLM for summarization of retrieved chunks 

`grade_prompt` - Prompt choice for model self-grading

**Blog**

https://blog.langchain.dev/auto-eval-of-question-answering-tasks/

**UI**

<img width="1440" alt="Screen Shot 2023-07-17 at 5 27 56 PM" src="https://github.com/huqianghui/auto-evaluator/assets/7360524/b2e474b6-b0bc-4f01-af36-89f2e4a8daaa">


**Disclaimer**

```I change from OpenAI to AzureOpenAI with access to `GPT-4` or `gpt-35-turbo` and an Anthropic API key to take advantage of all of the default dashboard model settings. However, additional models (e.g., from Hugging Face) can be easily added to the app.```
