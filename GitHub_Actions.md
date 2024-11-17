# GitHub Actions Cheatsheet

# Actions
Github Actions is a CI/CD pipeline directly integrated with our github repository.

We can:
- run test suites
- building images
- compiling static sites
- deploying code to servers

```yaml
name: Example Workflow
on: [push]
jobs:
	build:
		runs on: ubuntu-latest
		steps:
		- Users: actions/checkout@v2
		- name: Run a script
		  run: echo "This script runs on every push."
```

`on` contains event triggers which cause the github action to run.

Examples for event triggers (35+):
- pushes
- pull requests
- issues
- releases
- scheduled events
- manual triggers

# Workflows
configurable automated process that will run 1 or more jobs
defined by a YAML file in our repository
![alt text](<./assets/github_actions/Pasted image 20240728233000.png>)

## Triggering Scheduled Event
```yaml
on:
	schedule:
	- cron: '30 5 * * 1,3'
	- cron: '30 5 * * 2,4'
jobs:
	test_schedule:
		runs-on: ubuntu-latest
		steps:
			- name: Not on Monday or Wednesday
			  if: github.event.schedule != '30 5 * * 1,3'
			  run: echo "Skip this step on Monday and Wednesday"
			- name: Every time 
			  run: echo "This step will always run"
```

cron syntax - 
![alt text](<./assets/github_actions/Pasted image 20240728233720.png>)

If we specify multiple event triggers, only one of those events needs to occur to trigger the workflow.


## Runners

![alt text](<./assets/github_actions/Pasted image 20240729030214.png>)

## Workflow Commands

![alt text](<./assets/github_actions/Pasted image 20240729034328.png>)
![alt text](<./assets/github_actions/Pasted image 20240729034357.png>)


## Workflow Contexts
![alt text](<./assets/github_actions/Pasted image 20240729035134.png>)
`$GITHUB_ACTION` gives the action.
`$GITHUB_ACTOR` gives the username of the user triggering the action.
`$GITHUB_REPOSITORY` gives the name of the repo.
`$GITHUB_WORKFLOW`: gives the github workflow name.

### Secrets context - for sensitive info inside a workflow run
![alt text](<./assets/github_actions/Pasted image 20240729040557.png>)
`secrets.GITHUB_TOKEN` - at start of each workflow job, github automatically creates a unique GITHUB_TOKEN to use in our workflow for other jobs.
- we can use the GITHUB_TOKEN to authenticate in the workflow job when using APIs

### vars context - for non-sensitive variables at environment, repo, organization levels
![alt text](<./assets/github_actions/Pasted image 20240729040753.png>)
### env context - for variables at workflow, job or step level
![alt text](<./assets/github_actions/Pasted image 20240729041342.png>)


## Dependent Jobs
![alt text](<./assets/github_actions/Pasted image 20240729035902.png>)



## adding script to workflow
- we can execute bash scripts withing a workflow using ubuntu
- powershell in windows
![alt text](<./assets/github_actions/Pasted image 20240729042131.png>)


# Publishing Github Package using workflow
![alt text](<./assets/github_actions/Pasted image 20240729042524.png>)

# Publish components as github release
![alt text](<./assets/github_actions/Pasted image 20240729042811.png>)

# Deploy release to cloud provider
we can deploy to many cloud service providers
- Amazon Elastic Container Services (ECS)
- Google Kubernetes Engine
- Azure App Services, Azure Kubernetes Services (EKS), Azure static web apps

eg with Azure web app
![alt text](<./assets/github_actions/Pasted image 20240729043124.png>)

# Routing workflow to runner
A self hosted runner automatically receives certain labels when it is added to github actions
![alt text](<./assets/github_actions/Pasted image 20240729043546.png>)

we can group multiple runners too  and create a security boundary between them and they can be sent together with labels too.
```yaml
runs-on:
	group: ubuntu-runners
	labels: ubuntu-20.04-16core
```


# Caching package and dependency files
- makes workflows faster and improves performance
![alt text](<./assets/github_actions/Pasted image 20240729044100.png>)

# Job matrix configuration
A matrix strategy lets you use variables in a single job definition to automatically create multiple job runs that are based on the combinations of the variables. 
![alt text](<./assets/github_actions/Pasted image 20240729044614.png>)


# Disabling vs Deleting workflows
![alt text](<./assets/github_actions/Pasted image 20240729045048.png>)

# Types of actions
![alt text](<./assets/github_actions/Pasted image 20240729045151.png>)

### Files and Directories Scaffolding

1. JS Actions
	![alt text](<./assets/github_actions/Pasted image 20240729045658.png>)
	
2. Docker Container Actions
	!![alt text](<./assets/github_actions/Pasted image 20240729045758.png>)


# Exit codes for github actions
we can set exit codes so we can set status for an action by ourselves
![alt text](<./assets/github_actions/Pasted image 20240729045912.png>)


# Workflow Templates
*Enterprise feature* - to create reusable templates that other enterprise members can use.

**Note: only users with write access to the enterprise .github repo can create workflows from workflow templates** 

-- workflows
-- workflow templates
	- action.yml
	- action.json

Note: The workflow YML file and Metadata JSON file need to have the same name.
![alt text](<./assets/github_actions/Pasted image 20240729050433.png>)


# Workflow status badge
![alt text](<./assets/github_actions/Pasted image 20240729044342.png>)

