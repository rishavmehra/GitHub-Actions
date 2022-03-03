# GitHub-Actions

### What is GitHub Actions?
>We can automate, customize, and execute our software development workflows right in our repository with GitHub Actions. We can discover, create, and share actions to perform any job we need, including CI/CD, and combine actions in a completely customized workflow.
GitHub Actions are an automated process that allows us to build, test, release and deploy any code project on GitHub, but we can also use it to automate any step of our workflow such as merging pull requests, assigning levels, triaging issues etc
In short: GitHub Actions are a custom software developmet workflow automation tool

GitHub Action Components:

```
- WorkFLow
- ON Event
- JObs
- Runners
- Steps
- Matrix
- ENV
- Secrets
- Cache
```
#### WorkFLow

>Workflow is a configurable, automated process that we can use in our repository to build, test, package, release, or deploy your project. Workflows are made up of one or more “jobs" and can be triggered by GitHub events.

*Workflow Files:* 
Workflows can be created inside the .github/workflows directory by adding a .yml/.yaml workflow file. For example, add .github/workflows/build_and_deploy_action.yaml to your project. 
*Workflow Sytax:*
Github Actions files are written using YAML syntax and have either a .yml or .yaml file extension
*Workflow Name:* 
The name of your workflow is displayed on the Github actions page. If you omit this field, it is set to the file

#### On Event
>The on keyword defines the Github events that trigger the workflow. We can provide a single event, array, or events or a configuration map that schedules a workflow.


