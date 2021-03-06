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
* #### WorkFLow

>Workflow is a configurable, automated process that we can use in our repository to build, test, package, release, or deploy your project. Workflows are made up of one or more “jobs" and can be triggered by GitHub events.

*Workflow Files:* 
Workflows can be created inside the .github/workflows directory by adding a .yml/.yaml workflow file. For example, add .github/workflows/build_and_deploy_action.yaml to your project. </br>
*Workflow Sytax:*</br>
Github Actions files are written using YAML syntax and have either a .yml or .yaml file extension</br>
*Workflow Name:* </br>
The name of your workflow is displayed on the Github actions page. If you omit this field, it is set to the file</br>

* #### On Event
>The on keyword defines the Github events that trigger the workflow. We can provide a single event, array, or events or a configuration map that schedules a workflow.

* #### JObs

>A workflow run is made up of one or more jobs. Jobs define the functionality that will be run in the workflow and run in parallel by default.</br>

*Job Collection*</br>
A workflow usually consists of one or more jobs identified by unique job id (e.g. my-job), jobs ruins in parallel unless queued with the "needs" attribute. Each job runs in a fresh instance of the virtual environment specified by "runs-on"</br>
*Needs*</br>
Identifies any job that needs to be completed successfully before this job runs.</br>
*Runs-on*</br>
Type of Virtual Machine to run the job on. example: ubuntu-latest,windows-latest, macOS-latest.</br>

* #### Runners
> A runner is a machine with the Github Actions runner application installed. Then runner waits for available jobs it can then execute. After picking up a job they run the job's actions and report the progress and results back to Github. Runners can be hosted on Github or self-hosted on your own machines/servers.</br>

* #### Steps

>A Job contains a sequence of tasks called steps. Steps can run commands and actions.</br>

*Step Name*</br>
Specify the label to display for this step on GitHub 
*Uses*</br>
Specify an action to run as part of step in our workflow job 
*With*</br>
A map of input parameters is defined by the action in it's actions.yml file
*Run*</br>
Instead of running an existing action, a command-line program can be run using an operating system shell. Multiple commands can be run in a single shell instance by using "I" (pipe) operator

* #### Matrix
>A build matrix allows you to test across multiple operating systems, platforms, and language versions at the same time. You can specify a build matrix using the strategy keyword and pass it to runs-on.

#### ENV
> GitHub sets default environment variables for each GitHub Actions workflow run. We can also set custom environment variables in our workflow file using **"env"**

**Env**</br>
defines a map of environment variables that are available to all jobs and steps in the workflow. You can also set environment variables that are only available to a job or step.


#### Secrets

> Secrets are encrypted environment variables that we create in an organization, repository, or repository environment. The secrets that we create are available to use in GitHub Actions workflows. Sensitive values should never be stored as plaintext in workflow files, but rather as secrets

Secrets get accessed in workflow like this: **${{ secrets.SECRET_KEY_HERE }}**

#### Cache

>The workflow runs often reuse the same output as the previous ones and can therefore be cached for an increase in performance. Every job run on Github-hosted runners starts in a clean virtual environment and doesn't use cache by default.</br>
Caching is made possible by the Github cache action which will attempt to restore a cache based on the key you provide. If no match for the cache key is found it will create a new one after the successful completion of the job.
</br>

*Input parameters:*</br>
- key (Required): The key identifies the cache and is created when saving the cache. </br>
- path (Required): The file path of the directory you want to cache or restore. </br>
- restore-key (Optional): An ordered list of alternative keys to use for finding the cache if
no cache hit occurred for the key.</br> 

*Output parameters:*</br>
- cache-hit: Boolean variable with success state of the cache action</br>


Special *Thanks* to [@Njuchi_](https://twitter.com/Njuchi_) and [@techie_sandy](https://twitter.com/techie_sandy)