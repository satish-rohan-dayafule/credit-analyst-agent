
```markdown
# AI Credit Analyst Agent 🤖📊

## Overview
This project is an AI-powered pipeline designed to automate financial spreading, ratio calculation, and credit report generation. Built using **CrewAI**, the system utilizes a multi-agent architecture to read public SEC filings (10-K), extract key financial data, perform liquidity and profitability analysis, and output a formatted PDF Credit Portfolio Report.

This project bridges commercial banking domain expertise with Generative AI, demonstrating how LLMs can be orchestrated to scale and automate traditional credit risk assessment processes.

## Features
* **Multi-Agent Architecture:** Utilizes CrewAI to manage specialized agents (Data Extractor, Credit Analyst, Reporting Officer).
* **Automated Data Extraction:** Parses complex PDF financial statements (like Tesla's 10-K) to extract Balance Sheet and Income Statement data accurately.
* **Financial Ratio Calculation:** Automatically computes Current Ratio, Debt-to-Equity, Interest Coverage, and Net Margin based on the extracted data.
* **Generative Analysis:** Produces a concise, professional credit opinion evaluating liquidity and profitability.
* **PDF Generation:** Compiles the extracted data, ratios, and the AI-generated analysis into a clean, standardized PDF report using `fpdf`.

## Project Structure
* `Credit_AI_Agent_Code.ipynb`: The main Jupyter Notebook containing the agent configurations, tool definitions, and orchestration logic.
* `data/`: Directory for input PDF financial statements (contains a sample Tesla 2024 10-K).
* `extracted_financial_data.json`: The intermediate data file where the agents store and read the extracted numbers.

## Getting Started

### Prerequisites
* Python 3.8+
* An OpenAI API Key (GPT-4o-mini is used by default for cost-efficiency)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/satish-rohan-dayafule/credit-analyst-agent.git
   cd credit-analyst-agent

```

2. Install the required dependencies:
```bash
pip install crewai langchain-openai pypdf fpdf

```



### Usage

1. Open `Credit_AI_Agent_Code.ipynb` in your Jupyter environment.
2. Locate the `# 1. USER CONFIGURATION` section.
3. Replace `"YOUR_OPENAI_API_KEY_HERE"` with your actual OpenAI API key. **(Do not commit your API key to GitHub!)**
4. Ensure the `PDF_FILE_PATH` points to the target financial statement inside the data folder (e.g., `"data/tsla-20241231.pdf"`).
5. Run all cells in the notebook.
6. The final report will be generated as `Final_Credit_Report.pdf` in your working directory.

## Future Enhancements

* Integrate Langflow for a visual node-based UI.
* Implement dynamic SEC EDGAR API fetching to remove the need for manual PDF downloads.
* Expand ratio analysis to include efficiency and market value ratios.

## Disclaimer

*This project relies on publicly available SEC filings (e.g., Tesla Inc. 2024 10-K) for demonstration purposes. It does not contain any proprietary or confidential banking data.*

```
