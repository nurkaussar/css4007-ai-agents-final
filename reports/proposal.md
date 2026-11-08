## Project Proposal

### Project Title
AI Academic Advisor Agent

### Problem Description
University academic advisors receive thousands of emails daily, causing huge delays (up to 2–3 days) in responding to student inquiries about course schedules, credit requirements, and deadlines. This application solves the problem by providing an intelligent AI agent that has instant access to university data and can answer student questions immediately.

### Target Users
University students and academic advisors.

### Selected Difficulty
C — Intermediate (Agent that chooses and uses tools)

### Expected Functionality
- Conversational chat interface with LLM.
- Automatic tool selection by the LLM to fetch course details and student deadlines.
- Structured output validation and robust error handling for invalid course IDs.
- At least 8 comprehensive test cases.

### Proposed Functions
1. `get_course_info(course_id: str) -> dict` — Returns course title, credits, description, and exam date.
2. `get_student_deadlines(student_id: str) -> list` — Returns upcoming assignment and exam deadlines for a specific student.
3. `check_room_availability(room_name: str) -> dict` — Checks if a university classroom is free.

### Proposed Agent Tools
- `get_course_info`: The agent needs this tool when a student asks about course requirements or details.
- `get_student_deadlines`: The agent needs this tool to answer questions about upcoming homework or exams.

### Model Selection
Google Gemini API (Free tier) or OpenRouter free models supporting tool calling.

### Architecture
A modular Python application where the LLM acts as the core decision-maker, dynamically selecting and invoking mock university database tools, processing the results, and returning a concise, accurate answer to the student.

### Example Requests
1. "When is the exam for AI101 and how many credits is it?"
2. "What deadlines do I have this week for student ID S001?"
3. "Can you check if room 402 is available?"

### Evaluation Plan
We will implement at least 8 unit and integration tests covering successful tool calls, incorrect course IDs, tool execution failures, and LLM response validation.

### Weekly Milestones
- **Week 10:** Proposal and planning (Current)
- **Week 11:** Initial LLM integration and environment setup
- **Week 12:** Core application logic and mock university database
- **Week 13:** Tool integration (LLM tool-calling logic)
- **Week 14:** End-to-end workflow demonstration and error handling
- **Week 15:** Reliability improvements and test coverage expansion
- **Week 16:** Final testing, evaluation, and documentation
- **Week 17:** Final submission, defense, and demonstration
