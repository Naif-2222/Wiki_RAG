this projec is a simple RAG with 2 chunking stratigys 

Pulls a small corpus from Wikipedia

Chunks it two different ways

Embeds the chunks into a local vector database Chroma 

Runs a small LLM Qwen2.5-1.5B  inside the Colab env

Serves a Gradio UI that lets you pick the chunking strategy and see both the answer and the retrieved chunks side by side

The two chunking strategies

Recursive character splitter.

Splits on a hierarchy of separators paragraphs → lines → words → characters targeting 500 characters per chunk 
with 50 character overlap. 

Markdown header splitter.

Splits at #, ##, ### boundaries and preserves the header path as metadata. 

The two strategies are stored in separate Chroma collections so retrieval results can be compared directly in the UI.

Good Resources:

https://docs.langchain.com/oss/python/langchain/rag

https://www.deeplearning.ai/courses/building-evaluating-advanced-rag

https://www.pinecone.io/learn/retrieval-augmented-generation/

https://www.anthropic.com/engineering/contextual-retrieval

https://jalammar.github.io/illustrated-retrieval-transformer/

https://arxiv.org/abs/2412.15115

https://huggingface.co/docs/transformers/index
