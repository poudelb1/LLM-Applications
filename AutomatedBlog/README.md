## Final Project: Automated Blog Generation with CrewAI Agents

### 📚 What I Learnt  
- **Agentic workflows**: build a multi-agent pipeline (Researcher → Writer → Editor → Image) using the CrewAI framework.  
- **Tool integration**: leverage `SerperDevTool()` for Google search and `ScrapeWebsiteTool` for content extraction.  
- **LLM orchestration**: compare and select models (e.g., `googleGemini-1.5-flash` for drafting, OpenAI image APIs for visuals).  
- **Prompt chaining & refinement**: design prompts for each agent to ensure accuracy, coherence, and style consistency.  
- **End-to-end automation**: generate a polished blog post with a custom illustration and optionally schedule publishing via Sprout Social.

### 📂 Files & Notebooks  
- **`Project_Outline.pdf`**  
  Proposal detailing the project objective, scope (Researcher, Writer, Editor agents), frameworks (CrewAI, LangChain), and workflow steps citeturn1file0  
- **`blogCrew.ipynb`**  
  Core Colab notebook:  
  1. **Setup**: import libraries, configure API keys.  
  2. **Agent definitions**: instantiate and configure Researcher, Writer, Editor, and Image agents.  
  3. **Execution pipeline**: sequentially run agents to fetch research, draft content, refine text, and generate an image.  
  4. **Output**: final blog post (Markdown) and accompanying image file.  
- **`Sample Blogs.pdf`**  
  Example outputs for topics like “Role of AI in Healthcare,” “Rise of F1 in the US,” and more citeturn1file1  

### 🚀 How to Run  

1. **Install dependencies**  
   ```bash
   pip install crewai langchain openai serper-sdk
   ```  
2. **Configure your API keys**  
   ```bash
   export OPENAI_API_KEY="your_openai_key"
   export SERPER_API_KEY="your_serper_key"
   ```  
3. **Launch the notebook**  
   - Open `blogCrew.ipynb` in Colab or Jupyter.  
   - Run cells in order from top to bottom.  
4. **Generate a Blog**  
   - Set `topic = "<your topic here>"` in the first cell.  
   - Execute the pipeline:  
     1. **Researcher Agent** gathers the latest articles and compiles a 2‑paragraph report.  
     2. **Writer Agent** drafts a narrative using the report as context.  
     3. **Editor Agent** refines tone, structure, and clarity.  
     4. **Image Agent** creates a custom illustration for the post.  
   - View the final Markdown and image in the notebook’s output.  
5. **Customize & Extend**  
   - Swap in different LLMs (e.g., `gpt-4o`, `googleGemini-1.5-flash`).  
   - Adjust agent prompts in the notebook to fit your style.  
   - Integrate additional research tools or publishing APIs (e.g., Sprout Social).

---
