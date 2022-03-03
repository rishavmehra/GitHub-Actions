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
Workflows can be created inside the .github/workflows directory by adding a .yml/.yaml workflow file. For example, add .github/workflows/build_and_deploy_action.yaml to your project. </br>
*Workflow Sytax:*</br>
Github Actions files are written using YAML syntax and have either a .yml or .yaml file extension</br>
*Workflow Name:* </br>
The name of your workflow is displayed on the Github actions page. If you omit this field, it is set to the file</br>

#### On Event
>The on keyword defines the Github events that trigger the workflow. We can provide a single event, array, or events or a configuration map that schedules a workflow.

#### JObs

>A workflow run is made up of one or more jobs. Jobs define the functionality that will be run in the workflow and run in parallel by default.</br>

*Job Collection*</br>
A workflow usually consists of one or more jobs identified by unique job id (e.g. my-job), jobs ruins in parallel unless queued with the "needs" attribute. Each job runs in a fresh instance of the virtual environment specified by "runs-on"</br>
*Needs*</br>
Identifies any job that needs to be completed successfully before this job runs.</br>
*Runs-on*</br>
Type of Virtual Machine to run the job on. example: ubuntu-latest,windows-latest, macOS-latest.</br>

#### Runners
> A runner is a machine with the Github Actions runner application installed. Then runner waits for available jobs it can then execute. After picking up a job they run the job's actions and report the progress and results back to Github. Runners can be hosted on Github or self-hosted on your own machines/servers.</br>

#### Steps

>A Job contains a sequence of tasks called steps. Steps can run commands and actions.</br>

*Step Name*</br>
Specify the label to display for this step on GitHub 
*Uses*</br>
Specify an action to run as part of step in our workflow job 
*With*</br>
A map of input parameters is defined by the action in it's actions.yml file
*Run*</br>
Instead of running an existing action, a command-line program can be run using an operating system shell. Multiple commands can be run in a single shell instance by using "I" (pipe) operator

#### Matrix
