Steps to run the Agentic AI Code generation solution:

This code will automatically generate sql schema, design documentation, python code (api endpoints) and streamlit ui, all automatically by itself with zero human intervention. Basically full application and documentations created using ai with zero human intervention.

MAKE SURE YOU HAVE MIN PYTHON 3.11

setup new virtual environment- python -m venv venv

Activate venv: Mac: source venv/bin/activate Windows: .\venv\Scripts\activate

install requirements pip install 'crewai[tools]' python-dotenv langchain-openai Flask Flask-Cors streamlit requests

create .env file and add your openai api key: OPENAI_API_KEY=Your key here

python3 app.py

Agents used summary: Agent 1- The Architect(The Planner): First agent is Senior System Architect. It will provide detailed design document, figuring out what data to track, how the database should be structured and what API endpoints are needed. It basicaly created the blueprint for the whole operation

Agent 2- The DBA(The Foundation Builder): Once the blueprint is ready, the Database Administrator agent will read architects database schema and make it into a clean, functional schema.sql file. This agent's main focus is to create the foundation for our application data for all the tables and relationships

Agent 3- The Backend Dev (The Engineer): This agent's task is to prepare api endpoints. It used the design document and the SQL schema to build the entire Flask API. It wrote the code for every endpoint like registering students, marking attendance, handling feedback, and generating reports—turning the static design into a working code.

Agent 4- The Frontend Dev (The UI/UX Specialist): The Frontend Developer is used to build the ui. It analyzed the backend code to understand the available API endpoints and then built a streamlit application. This agent focused on creating a simple and intuitive UI, allowing a real user to click buttons, fill out forms, and see the reports, making the whole system usable.

Agent 5- The Technical Writer (The Documenter): Its job is to create documentations. It reviewed the work of all the other agents to provide clear instructions on what the project does, what features it has, and how to get it set up and running on your own machine.

All the agents interact together to provide fully functional, ready to use application with no human effort (effort put only to create this agentic ai solution). Using agentic ai methods, we can create agents who are masters of multiple technologies and make them work together to create any solutions.
