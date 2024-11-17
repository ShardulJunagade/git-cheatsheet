# GitHub Cheatsheet

**VCS - Version Control System**
- designed to track changes or revisions to code
	(eg- CVS, subversion, mercurial, git)

Git - Distributed version control system (DVCS)
![alt text](<./assets/github/Pasted image 20240627172901.png>)

Version Control Services (also called VCS)
- fully managed cloud services that host version controller repos
- eg- Github, GitLab, BitBucket, SourceForge

# Github
- Git repo hosting
- project management tools
- issue tracking
- pull requests and code review
- github pages and wikis
- github actions
- github copilot
- Codespaces, marketplace, gists, discussion
- collaboration features
- Github Desktop, CLI
- Github classroom
- security features

**Git vs Github**
![alt text](<./assets/github/Pasted image 20240627194152.png>)


**Github Flow**
![alt text](<./assets/github/Pasted image 20240628020727.png>)



**Github CLI**
Install the CLI for Windows
```sh
winget install --id GitHub.cli
```

**Configuration:**

- Run `gh auth login` to authenticate with your GitHub account. Alternatively, gh will respect the `GITHUB_TOKEN` environment variable.
- To set your preferred editor, use `gh config set editor <editor>`.
- Declare your aliases for often-used commands with `gh alias set`.


**SSH Keys**
![alt text](<./assets/github/Pasted image 20240628023410.png>)


**Deploy Keys**
![alt text](<./assets/github/Pasted image 20240628023512.png>)


**Personal Access Tokens (PAT)**
![alt text](<./assets/github/Pasted image 20240628023708.png>)


## REST vs GraphQL
![alt text](<./assets/github/Pasted image 20240628024711.png>)

## Github SDKs
Octokit- official SDKs to programmatically interact with the Git REST API
	supported languages- JS, TS, C#, .NET, Ruby, Terraform Provider

## Github Desktop vs Github
![alt text](<./assets/github/Pasted image 20240628035944.png>)


## Github Pesonal (Free vs Pro)
![alt text](<./assets/github/Pasted image 20240628040534.png>)

## Github Organizations (Free, Teams, Enterprise)
![alt text](<./assets/github/Pasted image 20240628040849.png>)
![alt text](<./assets/github/Pasted image 20240628041040.png>)


## Branches
![alt text](<./assets/github/Pasted image 20240628085044.png>)

## Feature Preview
- ==Ctrl+k  ----> opens command palette==
- slash commands
- colorblind themes
- jupyter notebook diffs


## Tagging
![alt text](<./assets/github/Pasted image 20240628091542.png>)


## Github Releases
Github Releases allows you to create releases with release notes and linked assets such as zip source or binaries for specific platforms.

## Github Packages
platform for hosting and managing packages, including containers and other dependencies

## Repo Insights
![alt text](<./assets/github/Pasted image 20240628094405.png>)

- pulse
![alt text](<./assets/github/Pasted image 20240628094614.png>)


## Issues
Issue Templates
![alt text](<./assets/github/Pasted image 20240628103534.png>)

## Pull Requests (PR)
- formal process to put forth changes that can be manually or automatically reviewed before its accepted to the base (main) branch.
![alt text](<./assets/github/Pasted image 20240628105323.png>)
![alt text](<./assets/github/Pasted image 20240628135305.png>)

### Code Review by CODEOWNERS file
![alt text](<./assets/github/Pasted image 20240628135514.png>)

### PR Templates
- similar to issue templates
- create a file in `.github/pull_request_template.md`
- for multiple templates, create them in folder called `.github/PULL_REQUEST_TEMPLATE`


## Discussions
![alt text](<./assets/github/Pasted image 20240628140538.png>)


## Gists
[Create a new Gist (github.com)](https://gist.github.com/)
- provide a simple way to share code snippets with others
- every gist is a git repository, which means it can be forked and cloned.
![alt text](<./assets/github/Pasted image 20240628141112.png>)

## Github Actions
![alt text](<./assets/github/Pasted image 20240628141445.png>)

## Copilot Individuals vs Business
![alt text](<./assets/github/Pasted image 20240628141704.png>)


## Codespaces
- cloud developer environment (CDE)
![alt text](<./assets/github/Pasted image 20240628142051.png>)


## Github.dev vs Codespaces
![alt text](<./assets/github/Pasted image 20240628142701.png>)


## Open Source
![alt text](<./assets/github/Pasted image 20240628142811.png>)

## Inner Source
![alt text](<./assets/github/Pasted image 20240628143101.png>)

## Opensource vs Innersource
![alt text](<./assets/github/Pasted image 20240628143213.png>)


## Github Projects
- planning and tracking tool when working on github repo
![alt text](<./assets/github/Pasted image 20240628143557.png>)



## Access Permissions

![alt text](<./assets/github/Pasted image 20240628143947.png>)
![alt text](<./assets/github/Pasted image 20240628144030.png>)
![alt text](<./assets/github/Pasted image 20240628144037.png>)



![alt text](<./assets/github/Pasted image 20240628144258.png>)


## Security Features
![alt text](<./assets/github/Pasted image 20240628144353.png>)



## EMUs
![alt text](<./assets/github/Pasted image 20240628144132.png>)

![alt text](<./assets/github/Pasted image 20240628144535.png>)