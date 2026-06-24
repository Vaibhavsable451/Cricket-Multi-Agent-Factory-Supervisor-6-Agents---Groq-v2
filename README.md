# Cricket-Multi-Agent-Factory-Supervisor-6-Agents---Groq-v2
🏏 Cricket Multi-Agent Factory (Supervisor + 6 Specialized Agents)

An AI-powered Cricket Intelligence System built with n8n, Groq LLM, and SerpAPI, using a Supervisor-Agent Architecture that routes user queries to specialized cricket agents for live scores, player statistics, fixtures, news, tactical analysis, and historical records.

🚀 Features

✅ Live Cricket Scores & Match Status
✅ Player Statistics & Records
✅ Match Schedules & Fixtures
✅ Latest Cricket News
✅ Match Predictions & Tactical Analysis
✅ Historical Records & World Cup History
✅ Multi-Agent Supervisor Routing
✅ Web Search Grounding with SerpAPI
✅ Groq-Powered Fast Inference
✅ Hallucination Reduction via Agent Validation

🏗️ System Architecture
                    USER
                      │
                      ▼
              SUPERVISOR AGENT
                      │
     ┌────────────────┼────────────────┐
     ▼                ▼                ▼
  SCORE-X          STATX           CHRONOS
 Live Scores    Player Stats      Fixtures

     ▼                ▼                ▼
  Search          Search           Search

     ▼                ▼                ▼
 Validation     Validation      Validation

     ┌────────────────┼────────────────┐
     ▼                ▼                ▼
   PULSE           TACTIX          ARCHIVE
    News          Analysis         History

                      │
                      ▼
                FINAL RESPONSE
🤖 Agent Responsibilities
Agent	Responsibility
SCORE-X	Live scores, current match status
STATX	Player stats, batting & bowling records
CHRONOS	Match schedules, venues, upcoming fixtures
PULSE	Latest cricket news and announcements
TACTIX	Match analysis, predictions, pitch reports
ARCHIVE	Historical records, rankings, World Cups
⚙️ Tech Stack
n8n
Groq
SerpAPI
JavaScript
HTTP Request Nodes
Multi-Agent Architecture
🔄 Workflow
Example Query
Who won the last Cricket World Cup?
Supervisor Routing
Supervisor → ARCHIVE
Agent Action
ARCHIVE → Web Search → Validation → Response
Final Answer
Australia won the 2023 ICC Cricket World Cup.
🛡️ Reliability Features
Mandatory Tool Usage

Every specialist agent:

MUST call Web Search before answering.
Error Handling
STATX_ERROR
SCORE_X_ERROR
CHRONOS_ERROR
PULSE_ERROR
TACTIX_ERROR
ARCHIVE_ERROR

If live data is unavailable, agents return errors instead of hallucinating.

Validation Layer

Checks for:

Empty Search Results
Invalid Responses
Unsupported Claims
Missing Statistics
Outdated Fixture Data
📂 Project Structure
Cricket-Multi-Agent-Factory/
│
├── Supervisor
│
├── Agents/
│   ├── SCORE-X
│   ├── STATX
│   ├── CHRONOS
│   ├── PULSE
│   ├── TACTIX
│   └── ARCHIVE
│
├── Search Layer
│
├── Validation Layer
│
└── n8n Workflow JSON
🎯 Sample Queries
Live Score
What's the live score of India vs Australia?
Player Stats
Virat Kohli ODI average
Fixtures
India next match
News
Latest news about Jasprit Bumrah
Analysis
Who is likely to win today's match?
History
Who won the 2011 Cricket World Cup?
📸 Screenshots

Add screenshots of:

Workflow Canvas
Supervisor Routing
Agent Responses
Search Results
Final Output
🔮 Future Improvements
Live Cricbuzz Integration
ESPN Cricinfo API Support
Match Win Probability Model
RAG-Based Cricket Knowledge Base
Voice Cricket Assistant
WhatsApp Cricket Bot
Telegram Cricket Bot
🌟 Why This Project?

This project demonstrates:

Agentic AI Systems
Multi-Agent Orchestration
Prompt Engineering
Tool Calling
Workflow Automation
Hallucination Reduction
Production-Ready AI Architecture
👨‍💻 Author
Vaibhav Sable

Generative AI Engineer

LLMs • RAG • AI Agents • LangChain • Python • FastAPI • Vector Databases
