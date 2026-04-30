--- 
name: octopus-deploy-agent
description: Helps users inspect, query, and diagnose Octopus Deploy instances
disable-model-invocation: true
tools: ["bash", "view", "edit"]
mcp-servers: 
  my-server: 
    type: stdio 
    args: ["-y", "@octopusdeploy/mcp-server"]
    env:
      OCTOPUS_API_KEY: "$OCTOPUS_API_KEY"
    tools: ["*"] 
    oidc: false
---
