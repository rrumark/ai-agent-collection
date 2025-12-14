# LLM Agent Collection 

- AI-powered agents capable of performing various tasks through natural language commands.
- Developed using the `phidata` and `groq` libraries.

This setup utilizes **Groq (llama-3.3-70b-versatile)**, offering a free API key with **1200 tokens/second** throughput.

## Key Features

- **File Manager Agent**: Enables file operations via natural language commands.
- **Finance Agent**: Provides insights and compares stocks/companies.
- **Search Agent**: Mainly used within other agents to retrieve relevant information from the web.
- **Teach Agent**: Summarizes YouTube videos based on your input.

## Prerequisites

### Required Libraries:
```bash
pip install phidata


## Configuration

#### Environment Variables (dotenv)

```bash
export GROQ_API_KEY = "YOUR_API_KEY"
$env:GROQ_API_KEY= "YOUR_API_KEY"
```
### Imports

```python
from phi.agent import Agent
from phi.model.groq import Groq

from phi.tools.duckduckgo import DuckDuckGo
from phi.tools.file import FileTools
from phi.tools.googlesearch import GoogleSearch
from phi.tools.crawl4ai_tools import Crawl4aiTools
from phi.tools.youtube_tools import YouTubeTools
from phi.tools.exa import ExaTools

from dotenv import load_dotenv

from bs4 import BeautifulSoup
import requests

load_dotenv()

```
## Examples

### File Manager Agent
```python

fileManager_agent.print_response("Find me 10 best coffee shops in London and save them in a new file", stream=True)

```

### Finance Agent
```python

finance_agent.print_response("Which stock is more likely to grow: AAPL or TSLA, based on the latest market news?", stream=True)

```

### Web-Content Agent
```python

web_agent.print_response("Can you explain how Blockchain works and its applications?", stream=True)

```

### Search Agent
```python

search_agent.print_response("What new AI products have been launched this month?", stream=True)

```

### Teach Agent
```python

study_partner.print_response("Summarize the latest Sam Altman video on YouTube", stream=True)

```

## Integrating Agents as Tools

- These agents can be seamlessly integrated into your projects as versatile tools.
- Building a team of specialized agents helps simplify decision-making when choosing the right agent for each task.
- You can further reduce hallucinations by implementing parallelization and tool routing strategies to enhance collaboration between agents.
- Check [https://github.com/openai/openai-agents-python] for more Agents as a tool implementation.




