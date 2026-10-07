# Job Application Agent

CrewAI agent that generates a complete job application package: cover letter, tailored resume bullets, interview questions, and salary range.

**Framework**: CrewAI  
**LLM**: Gemini 3.5-flash-lite 

## Environment Installation

```bash
pip install -r requirements.txt
```

## Configuration

Set your Gemini API key in the project-root `.env` file:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Do not commit this file; it is excluded by `.gitignore`.

## Structure 

```bash
python agent.py

# Your own job + profile
python agent.py \
  --job-desc "$(cat job_posting.txt)" \
  --candidate "$(cat my_profile.txt)"
```

## Output includes

- Tailored cover letter (250-300 words)
- Top 5 resume bullets to highlight
- Salary negotiation range
- 10 interview questions with answer frameworks