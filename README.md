# Assume-DataParser-for-LLM
This repository is a curated collection of open-source projects focused on document and web page parsing, specifically designed to facilitate the preprocessing of data for Large Language Models (LLMs).

## Opensource

### Traditional-model Based
- [PyMuPDF4LLM](https://pymupdf.readthedocs.io/en/latest/pymupdf4llm/)  
  PyMuPDF4LLM is aimed to make it easier to extract PDF content in the format you need for LLM & RAG environments. It supports Markdown extraction as well as LlamaIndex document output.

- [MinerU](https://github.com/opendatalab/MinerU)  
  MinerU is a tool that converts PDFs into machine-readable formats (e.g., markdown, JSON), allowing for easy extraction into any format.
MinerU was born during the pre-training process of [InternLM](https://github.com/InternLM/InternLM). We focus on solving symbol conversion issues in scientific literature and hope to contribute to technological development in the era of large models.
Compared to well-known commercial products, MinerU is still young. If you encounter any issues or if the results are not as expected.

- [Marker](https://github.com/VikParuchuri/marker)  
   Marker converts PDF to markdown quickly and accurately.  
    - Supports a wide range of documents (optimized for books and scientific papers)
    - Supports all languages
    - Removes headers/footers/other artifacts
    - Formats tables and code blocks
    - Extracts and saves images along with the markdown
    - Converts most equations to latex
    - Works on GPU, CPU, or MPS

- [unstructed](https://github.com/Unstructured-IO/unstructured)  
  The `unstructured` library provides open-source components for ingesting and pre-processing images and text documents, such as PDFs, HTML, Word docs, and [many more](https://docs.unstructured.io/open-source/core-functionality/partitioning). The use cases of `unstructured` revolve around streamlining and optimizing the data processing workflow for LLMs. `unstructured` modular functions and connectors form a cohesive system that simplifies data ingestion and pre-processing, making it adaptable to different platforms and efficient in transforming unstructured data into structured outputs.


### Large-model Based
- [OCR-2.0](https://github.com/Ucas-HaoranWei/GOT-OCR2.0)
  Traditional OCR systems (OCR-1.0) are increasingly unable to meet people's usage due to the growing demand for intelligent processing of man-made optical characters. In this paper, we collectively refer to all artificial optical signals (e.g., plain texts, math/molecular formulas, tables, charts, sheet music, and even geometric shapes) as "characters" and propose the General OCR Theory along with an excellent model, namely GOT, to promote the arrival of OCR-2.0. The GOT, with 580M parameters, is a unified, elegant, and end-to-end model, consisting of a high-compression encoder and a long-contexts decoder. As an OCR-2.0 model, GOT can handle all the above "characters" under various OCR tasks. On the input side, the model supports commonly used scene- and document-style images in slice and whole-page styles. On the output side, GOT can generate plain or formatted results (markdown/tikz/smiles/kern) via an easy prompt. Besides, the model enjoys interactive OCR features, i.e., region-level recognition guided by coordinates or colors. Furthermore, we also adapt dynamic resolution and multi-page OCR technologies to GOT for better practicality. In experiments, we provide sufficient results to prove the superiority of our model.  

- [PDF-Wukong](https://github.com/yh-hust/PDF-Wukong)  
  Document understanding is a challenging task to process and comprehend large amounts of textual and visual information. Recent advances in Large Language Models (LLMs) have significantly improved the performance of this task. However, existing methods typically focus on either plain text or a limited number of document images, struggling to handle long PDF documents with interleaved text and images, especially in academic papers. In this paper, we introduce PDF-WuKong, a multimodal large language model (MLLM) which is designed to enhance multimodal question-answering (QA) for long PDF documents. PDF-WuKong incorporates a sparse sampler that operates on both text and image representations, significantly improving the efficiency and capability of the MLLM. The sparse sampler is integrated with the MLLM's image encoder and selects the paragraphs or diagrams most pertinent to user queries for processing by the language model. To effectively train and evaluate our model, we construct PaperPDF, a dataset consisting of a broad collection of academic papers sourced from arXiv, multiple strategies are proposed to generate automatically 1M QA pairs along with their corresponding evidence sources. Experimental results demonstrate the superiority and high efficiency of our approach over other models on the task of long multimodal PDF understanding, surpassing proprietary products by an average of 8.6% on F1.


### LLM/MLM Based
- [open-parse](https://github.com/Filimoa/open-parse)  
  Easily chunk complex documents the same way a human would.  
  Chunking documents is a challenging task that underpins any RAG system. High quality results are critical to a sucessful AI application, yet most open-source libraries are limited in their ability to handle complex documents.  
  Open Parse is designed to fill this gap by providing a flexible, easy-to-use library capable of visually discerning document layouts and chunking them effectively.
- [gptpdf](https://github.com/CosmosShadow/gptpdf)  
  Using VLLM (like GPT-4o) to parse PDF into markdown.
  Our approach is very simple (only 293 lines of code), but can almost perfectly parse typography, math formulas, tables, pictures, charts, etc. Average cost per page: $0.013
- [Crawl4AI](https://github.com/unclecode/crawl4ai)  
  Crawl4AI simplifies asynchronous web crawling and data extraction, making it accessible for large language models (LLMs) and AI applications.


## API server
- [chunkr](https://github.com/lumina-ai-inc/chunkr)  
  We're Lumina. We've built a search engine that's five times more relevant than Google Scholar. You can check us out at [lumina.sh](https://www.lumina.sh). We achieved this by bringing state-of-the-art search technology (the best in dense and sparse vector embeddings) to academic research.   
While search is one problem, sourcing high-quality data is another. We needed to process millions of PDFs in-house to build Lumina, and we found that existing solutions to extract structured information from PDFs were too slow and too expensive ($$ per page).   
Chunk my docs provides a self-hostable solution that leverages state-of-the-art (SOTA) vision models for segment extraction and OCR, unifying the output through a Rust Actix server. This setup allows you to process PDFs and extract segments at an impressive speed of approximately 5 pages per second on a single NVIDIA L4 instance, offering a cost-effective and scalable solution for high-accuracy bounding box segment extraction and OCR. This solution has models that accommodate both GPU and CPU environments. Try the UI on [chunkr.ai](https://www.chunkr.ai)!
- [Chatdoc-pdfparse](https://pdfparser.io/)  
  [ChatDOC PDF Parser vs. LlamaParse: Which One Is Superior?](https://medium.com/@chatdocai/chatdoc-pdf-parser-vs-llamaparse-which-one-is-superior-84844502164a)

