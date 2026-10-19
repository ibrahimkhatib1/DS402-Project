# Mini Course Agent

Repository: https://github.com/ibrahimkhatib1/DS402-Project

## Project goal

The Mini Course Agent gives students concise, source-grounded answers about assignments, course policies, and grade calculations. It uses OpenAI for reasoning and three controlled local tools for course data.

## Contributor

- Ibrahim Khatib - project owner, developer, tester, and documentation author

## Automated workflows

1. Find upcoming or submitted assignments.
2. Search approved course policies for late work, attendance, AI use, and grading.
3. Calculate percentages and basic course-related arithmetic.
4. Answer general course questions without calling a tool when no private course fact is needed.

## Integrated data and services

- OpenAI Agents SDK and OpenAI API
- Local assignment dataset in `src/mini_course_agent.py`
- Local approved course-policy dataset in `src/mini_course_agent.py`
- Safe arithmetic tool using Python's abstract syntax tree

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env.local
```

Add `OPENAI_API_KEY` to `.env.local`. Never commit that file.

## Run

```bash
python src/mini_course_agent.py "What assignment is due next?"
```

## Test

```bash
python -m unittest discover -s tests -v
```

## Security controls

- Blocks requests for system prompts, credentials, or another student's records.
- Uses a strict allowlist for tool inputs.
- Evaluates arithmetic without `eval()`.
- Keeps API keys in ignored environment files.
- Refuses to invent missing policy or assignment information.

