# DevOps-AI-Agent

DevOps-AI-Agent is a collection of example agents and helper code that demonstrate how to build AI-powered DevOps assistants which integrate GitHub activity, Grafana metrics, and serverless components. The repository contains Jupyter notebooks, Lambda function examples, and infrastructure scaffolding for experimenting with agents that supervise, correlate, and act on CI/CD and runtime signals.

**Quick links**
- **Source:** [devops_agent](devops_agent)
- **Notebooks:** [devops_agent](devops_agent)

**Repository layout**
- `devops_agent/`: Agent code, notebooks, examples, and templates.
	- `01_Create_Grafana_Assistant_Agent/`, `02_Create_GitHub_Assistant_Agent/`, `03_Create_Supervisor_Devops_Agent/`: example notebooks and supporting files.
	- `lambda_function.py`, `lambda_requirements.txt`: example Lambda code used by some notebooks.
	- `devops.properties.template`: configuration template for Grafana and GitHub credentials.
- `00_Setup_Instructions/cdk-app/`: sample AWS CDK app scaffold (TypeScript).

**Prerequisites**
- Python 3.8+ and `pip`.
- Optional: Node.js and AWS CDK if you plan to run the CDK app.
- A Grafana instance and a GitHub personal access token for integrations used by the notebooks.

**Quickstart**
1. Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install the Python dependencies used by the examples:

```bash
pip install -r devops_agent/requirements.txt
```

3. Copy the configuration template and fill in credentials:

```bash
cp devops_agent/devops.properties.template devops_agent/devops.properties
# Edit devops_agent/devops.properties and set grafana.url, grafana.token, github.token
```

4. Open the Jupyter notebooks and run the examples (recommended):

```bash
pip install notebook
jupyter notebook devops_agent/invoke_agent.ipynb
```

5. Explore the example notebooks in:

- [devops_agent/01_Create_Grafana_Assistant_Agent](devops_agent/01_Create_Grafana_Assistant_Agent)
- [devops_agent/02_Create_GitHub_Assistant_Agent](devops_agent/02_Create_GitHub_Assistant_Agent)
- [devops_agent/03_Create_Supervisor_Devops_Agent](devops_agent/03_Create_Supervisor_Devops_Agent)

**Notes**
- The `devops.properties.template` file contains placeholder keys required by the notebooks — do not commit secrets to version control.
- Lambda examples are provided in the agent subfolders and can be packaged/deployed separately; see corresponding `lambda_requirements.txt` files.

**Authors & License**
- Authors: Gene Ting, Bharath Sridharan, Rachna Chadha, Maira Ladeira Tanke
- License: Apache-2.0

If you'd like, I can also:
- run the notebooks end-to-end (if you give permission to install/execute), or
- update any notebook README sections with specific example outputs.

