# AI Research Crew

An automated research system that uses two specialized AI agents to research any topic and generate comprehensive reports. Currently configured to research **Artificial Intelligence in Telecommunications**.

## What This Does

🔍 **Researcher Agent** (Perplexity AI) → Gathers comprehensive information from the web  
📊 **Analyst Agent** (OpenAI GPT-4.1) → Creates professional reports with insights and analysis

### Why These Models?

**Perplexity for Research**: Excels at real-time web search and accessing current information with built-in citation capabilities. Perfect for gathering up-to-date facts and data.

**OpenAI for Analysis**: Superior at structured thinking, report writing, and synthesizing complex information into clear, professional documents.

## Quick Setup

### 1. Prerequisites
- Python 3.10+ installed
- [Get Perplexity API key](https://docs.perplexity.ai/docs/getting-started) (for research)
- [Get OpenAI API key](https://platform.openai.com/api-keys) (for analysis)

### 2. Install Dependencies
```bash
pip install uv
crewai install
```

### 3. Configure API Keys
Create/edit the `.env` file:
```bash
PERPLEXITY_API_KEY=your_perplexity_key_here
OPENAI_API_KEY=your_openai_key_here
SERPER_API_KEY=your_serper_key_here  # For web search
```

### 4. Run the Research
```bash
crewai run
```

## Output

The system generates a detailed research report saved to `output/report.md` covering:
- Executive summary
- Key concepts and definitions  
- Historical development and trends
- Challenges and opportunities
- Real-world applications
- Future outlook

## How It Works

1. **Research Phase**: Perplexity AI searches and analyzes web sources
2. **Analysis Phase**: OpenAI processes findings and creates structured report  
3. **Output**: Professional markdown report in `output/report.md`

## Change Research Topic

To research a different topic:
1. Open `src/research_crew/main.py`
2. Look for the line: `'topic': 'Artificial Intelligence in Telecommunications'`
3. Change it to your topic: `'topic': 'Machine Learning in Healthcare'`
4. Run `crewai run` again

## Optional: Customize Agents (Advanced)

If you want to modify what the agents do, you can edit these files:
- `src/research_crew/config/agents.yaml` - Change agent roles and goals
- `src/research_crew/config/tasks.yaml` - Modify what tasks they perform

## Learn More

Built with [CrewAI](https://docs.crewai.com/en/guides/crews/first-crew) - A framework for orchestrating AI agents.
