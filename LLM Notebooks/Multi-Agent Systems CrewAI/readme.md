### Project: [Customer Outreach with AI Agents:](https://github.com/xandie985/ai-buffet/blob/main/LLM%20Notebooks/Multi-Agent%20Systems%20CrewAI/automated%20customer%20outreach%20via%20agents.ipynb) A Streamlined Approach
 
**Goal:** Automate personalized customer outreach using AI agents.

**Process:**

1. **Lead Identification:** The Sales Representative Agent analyzes data and trends to identify high-value leads.
2. **Lead Profiling:** The agent gathers in-depth information about the company and decision-makers.
3. **Personalized Outreach:** The Lead Sales Representative Agent crafts tailored email drafts, incorporating insights from the profile. 
4. **Sentiment Analysis:** A custom tool ensures the message is positive and engaging.

**Key Tools:**

* DirectoryReadTool (reads instructions)
* FileReadTool
* SerperDevTool (web search)
* SentimentAnalysisTool (custom tool)

**Benefits:**

* Efficiently identifies and targets high-value leads.
* Creates personalized, compelling outreach messages.
* Improves engagement and conversion rates.

---
### [Research and Article Writing AI Agents](https://github.com/xandie985/ai-buffet/blob/main/LLM%20Notebooks/Multi-Agent%20Systems%20CrewAI/automated%20article%20writing%20via%20agents.ipynb): Project Overview

**Objective:**

Develop a system using AI agents to streamline the process of researching and writing articles, leveraging their specialized roles and collaborative capabilities.

**Agents:**

*   **Content Planner:**  Researches the topic, identifies target audience, and creates an outline with SEO keywords.
*   **Content Writer:**  Uses the outline and research to craft an engaging, informative article.
*   **Editor:** Proofreads and refines the article to ensure quality and adherence to the brand's voice.

**Tasks:**

1.  **Plan:** Prioritize trends, identify audience, develop outline, and include relevant resources.
2.  **Write:** Craft a well-structured article using the plan, incorporating SEO keywords naturally.
3.  **Edit:** Proofread and ensure the article aligns with journalistic standards and the brand's voice.

**Workflow:**

1.  User provides the article topic.
2.  Content Planner agent gathers information and creates a comprehensive plan.
3.  Content Writer agent uses the plan to draft the article.
4.  Editor agent reviews and refines the article.
5.  The system outputs the final polished article.

**Key Points:**

*   Demonstrates the power of multi-agent collaboration in content creation.
*   Leverages LLMs' abilities in research, writing, and editing.
*   Emphasizes the importance of structure, SEO, and brand voice in article creation.
*   Showcases the potential of AI to automate and streamline content workflows.

---
### [Multi-Agent Customer Support Project](https://github.com/xandie985/ai-buffet/blob/main/LLM%20Notebooks/Multi-Agent%20Systems%20CrewAI/automated%20customer%20support%20via%20multi-agents.ipynb)

**Overview:**

This project showcases a multi-agent system for customer support, highlighting concepts like role-playing, focus, cooperation, tools, guardrails, and memory. Two agents collaborate to address customer inquiries efficiently and accurately.

**Agents:**

*   **Senior Support Representative:**  Provides friendly and helpful support, aiming to resolve customer inquiries completely.
*   **Support Quality Assurance Specialist:** Reviews the support representative's response to ensure quality and adherence to standards.

**Key Features:**

*   **Role Playing:** Agents are assigned specific roles with detailed backstories to guide their behavior and responses.
*   **Focus:** Agents stay on task by addressing all aspects of the inquiry and avoiding assumptions.
*   **Tools:** Agents use tools like the ScrapeWebsiteTool to access external knowledge sources (e.g., documentation) for accurate answers.
*   **Cooperation:** The QA agent reviews and refines the support agent's response, ensuring high quality and complete information.
*   **Guardrails:** The system ensures agents stay within their defined roles and generate appropriate responses.
*   **Memory:** Short-term and long-term memory enable agents to share context and learn from past interactions for continuous improvement.

**Workflow:**

1.  **Customer Inquiry:**  The customer submits an inquiry.
2.  **Inquiry Resolution:** The Support Agent uses tools to gather information and craft a detailed response.
3.  **Quality Assurance:** The QA Agent reviews the response, verifies accuracy, and suggests improvements.
4.  **Final Response:**  The refined response is sent to the customer.

**Additional Notes:**

*   This example uses `gpt-3.5-turbo`, but `gpt-4-turbo` could be used for even better performance.
*   Custom tools can be created to load customer data, access previous conversations, or integrate with CRMs.
*   The system demonstrates how AI agents can collaborate effectively to deliver high-quality customer support.
---
### [AI-Powered Event Management Crew](https://github.com/xandie985/ai-buffet/blob/main/LLM%20Notebooks/Multi-Agent%20Systems%20CrewAI/automated%20event%20planner%20via%20agents.ipynb)

**Goal:** Automate various aspects of event planning and management using a team of specialized AI agents.

**Agents:**

*   Venue Coordinator: Finds and books a suitable venue based on event requirements.
*   Logistics Manager: Handles catering and equipment logistics.
*   Marketing and Communications Agent: Promotes the event and communicates with participants.

**Tools:**

*   ScrapeWebsiteTool: Scrapes information from websites.
*   SerperDevTool: Performs web searches.

**Tasks:**

1.  **Venue Booking:** The Venue Coordinator searches for and selects a venue that aligns with the event's needs.
2.  **Logistics Coordination:** The Logistics Manager arranges catering and equipment for the specified number of participants and date.
3.  **Marketing and Promotion:** The Marketing and Communications Agent develops a strategy to reach the target audience and generate interest.

**Output:**

*   `venue_details.json`: Contains details about the selected venue (name, address, capacity, booking status).
*   `marketing_report.md`: Provides a summary of marketing activities and attendee engagement.

**Workflow:**

1.  User inputs event details (topic, description, city, date, expected participants, budget, venue type).
2.  Agents execute their tasks concurrently using the provided tools.
3.  The system generates output files with venue details and a marketing report.

**Key Points:**

*   Leverages crewAI framework for multi-agent collaboration.
*   Integrates custom tools (e.g., SentimentAnalysisTool) with external tools (e.g., SerperDevTool) for enhanced functionality.
*   Emphasizes automation and efficiency in event management.
*   Produces structured output (JSON, Markdown) for easy integration with other systems.
*   Showcases potential applications of AI in streamlining complex real-world tasks.
*   Asynchronous task execution is made possible with the async_execution parameter.
*   The pydantic object "VenueDetails" structures and validates venue information.
*   Human input option allows for feedback and refinement before finalizing tasks.
*   The project can be extended to utilize other LangChain tools for added functionality.

**Note:** In this specific example, the project's execution was limited due to an issue with the SerpApi, preventing web searches and scraping. However, the project successfully demonstrates the core concepts and potential of AI-driven event management.

---

![Alt text](image.png)

Generic Approach for Data Collection and Analysis:
![Alt text](image-1.png)

Outsmarting generic approaches using Agents
![Alt text](image-2.png)


Agents we would we dealing with:
1. Tech Job Researcher
2. Personal Profiler
3. Resume Strategist
4. Interview Preparation Expert

Steps to take:
- Search the internet
- Read websites
- Read resume
- Perform RAG on resume

---
## 1: AI Agents
![Alt text](image-4.png)
* **Definition:** Used to augment language models' capabilities beyond text generation, enabling them to interact with external tools and perform complex tasks.
* **Structure:** Often consist of:
    * LLM: The "brain" for understanding and generating language.
    * Tools: External functionalities the agent can access (e.g., calculators, search engines).
    * Memory: Stores information from past interactions.
    * Planner: Decides which actions to take based on the current situation and goal.

**Multi-Agents:**
![Alt text](image-5.png)
* **Definition:** Allows for more specialized agents working together, each with specific expertise (e.g., one for information retrieval, another for summarization), these agents can also be based on diffrent LLMs. 
* **Benefits:**
    * Improved efficiency and scalability.
    * Increased robustness and adaptability to complex problems.
    * Potential for emergent behavior and collective intelligence.

**Working Principle:**

1. **Perception:** Agents receive input from their environment (e.g., user query, context, tools).
2. **Reasoning:**  LLM processes input, utilizes memory, and potentially consults other agents to formulate a plan.
3. **Action:** Agent executes actions based on the plan (e.g., generate text, call a tool, communicate with another agent).
4. **Feedback:** Agent observes the results of its actions and updates its knowledge or strategy accordingly.

**Challenges:**

* **Coordination:** Designing effective communication and coordination mechanisms between agents.
* **Scalability:**  Managing the complexity of large-scale multi-agent systems.
* **Evaluation:** Measuring the performance and effectiveness of multi-agent systems.
* **Alignment:** Ensuring agents' goals align with human values and safety concerns.

---
## 2: Agents does the research and writes article for you. 
![Alt text](image-6.png)
This script sets up a system to automate the creation of blog articles using AI agents. It begins by installing necessary libraries and configuring the environment with an OpenAI API key. Three agents are defined: a Planner, a Writer, and an Editor, each with specific roles, goals, and backstories to enhance the performance of Large Language Models (LLMs) through role-playing. Tasks are then created for each agent, detailing the steps and expected outputs for planning, writing, and editing a blog post on a given topic. Finally, a Crew is assembled to manage the sequence of tasks, ensuring they are executed in the correct order, and the process is initiated with a specific topic input, generating a blog post on "Transformers and Attention in LLMs".

---
## 3. Key Elements in Agent
![Alt text](image-3.png)
AI Agent Characteristics:

| Characteristic | Description                                                                                                  | Importance                                                                                                                                      | Example in CrewAI |
|----------------|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| **Role Playing**    | Defining the agent's persona, goals, and backstory to guide its behavior and responses.                           | Helps agents produce specific, contextually appropriate outcomes; enables better control over agent behavior.                                   | Using keywords like "FINRA approved financial analyst" to achieve better financial analysis than "finacial analyst" alone. |
| **Focus**          | Limiting the agent's scope in terms of tools, information, and context to prevent information overload and hallucinations. | Ensures agents stay on task and produce accurate results, especially important for smaller models with limited capacity.                       | Multiple specialized agents instead of one generalist agent. |
| **Tools**          | Providing agents with the right tools for their tasks, avoiding overwhelming them with unnecessary options.            | Ensures agents have the necessary resources to perform their tasks effectively and efficiently.                                                | Giving an agent access to a calculator for mathematical tasks. |
| **Cooperation**   | Enabling agents to collaborate, share feedback, and delegate tasks.                                               | Leads to better outcomes through shared context, feedback, and task delegation.                                                               | Agents sharing learnings in a shared short-term memory during crew execution. |
| **Guardrails**      | Implementing safeguards to prevent hallucinations, loops, and other undesirable behaviors.                      | Ensures reliability, consistency, and safety in AI applications by preventing errors and keeping agents on track.                                 | Preventing agents from repeatedly using the same tool. |
| **Memory**         | The ability of agents to remember past actions, learn from them, and apply knowledge to future tasks.               | Significantly improves agent reliability and enables continuous improvement of outcomes over time.                                            | Short-term, long-term, and entity memory types in CrewAI. |


---
## 4. THings to keep in mind while working with Agents
![Alt text](image-7.png)

## 5. Tools
![Alt text](image-8.png)

Versatile:
![Alt text](image-11.png)
Fault-Tolerant:
![Alt text](image-10.png)
Caching:
![Alt text](image-9.png)
**Key Points about Tools in Multi-Agent Systems:**

* **Tools:** Allow AI agents to interact with the external world (APIs, databases, notifications, etc.).
* **Importance:** Crucial for real-world impact and application of multi-agent systems.
* **Qualities of Great Tools:**
    * Versatile: Handle diverse requests from LLMs.
    * Fault-tolerant: Fail gracefully without stopping execution.
    * Caching: Prevent unnecessary requests and save time/resources.
* **CrewAI Tools:**
    * Versatile, fault-tolerant, and implement smart caching.
    * Offers documentation for existing tools.
    * Supports LangChain tools for broader functionality.

**Key Takeaways:**

* Tools are a cornerstone of multi-agent systems.
* Choose tools mindfully, balancing capabilities with the agent's needs.
* Consider versatility, fault tolerance, and caching when building custom tools.
* Explore existing tool documentation for efficient development.

**Some important tools:**
Google Serper Search 
CSV RAG Search
Scrape Website
XML RAG Search
Directory Read
JSON RAG Search
File Read
Docx Rag Search
Selenium Scraper
MDX RAG Search
Directory RAG Search 
PG RAG Search
PDF RAG Search
Website RAG Search
TXT RAG Search
Github RAG Search
Code Docs RAG Search
Youtube Video RAG Youtube
Channel RAG Search