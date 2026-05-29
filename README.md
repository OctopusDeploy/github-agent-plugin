<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/octopusdeploy/mcp-server/blob/main/images/OctopusDeploy_Logo_DarkMode.png?raw=true">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/octopusdeploy/mcp-server/blob/main/images/OctopusDeploy_Logo_LightMode.png?raw=true">
  <img alt="Octopus Deploy Logo" src="https://github.com/octopusdeploy/mcp-server/blob/main/images/OctopusDeploy_Logo_LightMode.png?raw=true" />
</picture>

# Github Agent Plugin for Octopus Deploy

[Octopus](https://octopus.com) makes it easy to deliver software to Kubernetes, multi-cloud, on-prem infrastructure, and anywhere else. Automate the release, deployment, and operations of your software and AI workloads with a tool that can handle CD at scale in ways no other tool can.

Github Agent Plugin combines the power of the [Octopus MCP Server](https://github.com/OctopusDeploy/mcp-server) and a specialized set of skills to enable agents in Github Agent HQ and Copilot CLI to interact with Octopus Deploy in an automated fashion.

The MCP connects directly to your Octopus instance and can perform most actions that a regular user can:
- Create projects and deployment processes
- Create releases
- Execute runbooks
- Configure project variables
- Find any interruptions requiring human attention
- Inspect audit log
- And much more

The plugin comes with a set of skills to help with:
- Connecting a repository to Octopus
- Writing OCL ([Octopus Configuration Language](https://octopus.com/docs/projects/version-control/ocl-file-format))
- Diagnosing deployment failures and fixing them
- Producing an SOC2 audit report

## Getting Started

- Install `Octopus Deploy Intelligence Agent` Github App into your repository
- For each repository configure MCP secrets (**Secrets and variables -> Agents** to connect to your Octopus instance:
- `COPILOT_MCP_OCTOPUS_API_KEY` - an API key to connect to Octopus. We recommend setting up a separate [service account](https://octopus.com/docs/security/users-and-teams/service-accounts) with restricted permissions per Space.
- `COPILOT_MCP_OCTOPUS_SERVER_URL` - public URL for your instance, for example `https://myinstance.octopus.app`
- Invoke the agent by either going to **Agents** tab in your repository, or by mentioning the agent via `@` in PR or issue comments.

## Examples

Here is an example of what you can do with the Octopus Intelligence Agent:
📊 **Show me the deployment status of this PR, and when it was deployed to tenant X**
🔍 **Investigate and diagnose why it has failed**
🔧 **Use the appropriate runbook to fix the failure**
🚀 **Redeploy to tenant**
