# Exercise 1

Selected language - Go

### lint

For linting go source code there is a open-soruce project called `golangci-lint.run`  
Developers claim it's fast, colorful, has a lot of linters out of the box, reliable and easy to integrate into IDE and CI runners.  
Linter like this not only keep the codebase written by different people consistent, but also helps to prevent writing error prone code and introducing technical debt.

Another type of liner you could expect to appear in enterprise projects CI - is commitlint (https://commitlint.js.org/)  
It `helps your team adhere to a commit convention` which is helpful to automate building changelog when releasing new software version.  
Commit convention helps team to add more semantic to the history by using predefined commit convention. It might differ from project to project, but usually follows this pattern:

```
type(scope?): subject
body?
footer?
```

Additional check in pipeline might include check for copyright notice in the source files.

### Build & Test

For building and testing go projects, `go build` and `go test` commands are used.  
Those tests might be ran on Jenkins, github-hosted runners (github actions), gitlab-hosted runners or self-hosted runners on any of the platforms.

## Jenkins and github alternatives

Alternative to Jenkins and github for establishing CI/CD is Gitlab (which includes self-hosted runners in free tier), Bitbucket Pipeline and Travis CI.

Circle CI is also one of the services that I heard before as an alternative platform for running pipelines.

## Self-hosted vs managed runners.

In my believe the decision should be data-driven and include security risks that arise from using self-hosted runners, costs of maintanance and keeping self-hosted runners up and running.  
On the other hand, there is no alternative to self-hosted runners due to specific testing / building requrements of the project. Than it's easier to make a decision.
