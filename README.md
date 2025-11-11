# Deep Research Agent

An AI-powered research agent that performs comprehensive web research on any topic, synthesizes findings into detailed reports, and optionally sends them via email.

## Features

- **Intelligent Search Planning**: Uses AI to plan multiple targeted web searches based on your query
- **Parallel Web Search**: Performs multiple searches concurrently for efficiency
- **Report Generation**: Synthesizes search results into comprehensive, well-structured markdown reports
- **Email Integration**: Optionally sends formatted reports via email using SendGrid
- **Tracing & Debugging**: Built-in tracing capabilities to monitor agent behavior

## How It Works

1. **Planning Phase**: A planner agent analyzes your query and creates a strategic search plan with multiple search terms
2. **Search Phase**: Multiple search agents execute web searches in parallel based on the plan
3. **Writing Phase**: A writer agent synthesizes all search results into a detailed markdown report
4. **Email Phase** (Optional): An email agent formats and sends the report via email

## Installation

1. Clone this repository:
```bash
git clone https://github.com/Ayu369-gen/Deep-research-agent.git
cd Deep-research-agent
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
   - Create a `.env` file in the root directory
   - Add your API keys:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   SENDGRID_API_KEY=your_sendgrid_api_key_here
   ```

## Usage

### Basic Usage

Edit the `query` variable in `agent.py` (line 157) to your research topic:

```python
query = "Latest AI Agent frameworks in 2025"
```

Then run the script:

```python
python agent.py
```

### Running in Jupyter/IPython

The code is designed to work in Jupyter notebooks. You can run it cell by cell or as a complete script.

### Customizing Email Settings

Update the email addresses in the `send_email` function (lines 77-78):

```python
from_email = Email("your-email@example.com")  # Your verified SendGrid email
to_email = To("recipient@example.com")  # Recipient email
```

## Configuration

### Search Parameters

- `HOW_MANY_SEARCHES`: Number of searches to perform (default: 3)
- `search_context_size`: Web search context size ("low", "medium", or "high")
- Model: Currently using `gpt-4o-mini` for all agents

### Report Settings

- Report length: 5-10 pages (1000+ words)
- Format: Markdown
- Includes: Short summary, detailed report, and follow-up questions

## Dependencies

- **agents**: AI agent framework (see requirements.txt for specific package)
- **pydantic**: Data validation and settings management
- **python-dotenv**: Environment variable management
- **sendgrid**: Email sending service
- **IPython**: Interactive Python shell (optional, for Jupyter)

## Project Structure

```
Deep-research-agent/
├── agent.py           # Main research agent implementation
├── requirements.txt   # Python dependencies
├── README.md         # This file
└── .env              # Environment variables (create this)
```

## Important Notes

- **API Costs**: WebSearchTool incurs API charges. Monitor your usage.
- **SendGrid Setup**: You need a verified SendGrid account and API key
- **OpenAI API**: Requires an OpenAI API key with access to GPT-4 models
- **Async Execution**: The code uses async/await patterns for concurrent operations

## Example Output

The agent will:
1. Plan 3+ targeted searches
2. Execute searches in parallel
3. Generate a comprehensive markdown report with:
   - Short summary
   - Detailed findings (1000+ words)
   - Follow-up research questions
4. Send the report via email (if configured)

## Troubleshooting

### Import Errors
If you encounter import errors for the `agents` package, ensure it's properly installed:
```bash
pip install agents
```
If the package name differs, check the package documentation.

### Environment Variables
Make sure your `.env` file is in the root directory and contains all required API keys.

### Email Issues
- Verify your SendGrid API key is correct
- Ensure the sender email is verified in SendGrid
- Check SendGrid account limits

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Contact

[Your contact information]


