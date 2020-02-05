# gradle-test
This is a repo to try out various automation and git workflows with gradle.

## Why

- With our current git workflow I believe we run the risk of rushing pushes to master
    and having code with bugs or that does not compile during presentations.
- My proposal to help this is a modification where instead of rebasing and pushing directly
    to master, we push our local feature branch to a corresponding remote feature branch
    and then open a pull request to master.
- This modification opens the opportunity to do code reviews and testing before we
    update the code which will be used in critical demonstrations (presentations mostly).

## Gradle

- Gradle is a tool that can manage our builds, dependencies (Like JavaFX and JUnit), test runs, formatting, documentation,
    and more.
- It was recommended by our TA and seems to be a very popular choice for Java projects.
- Using Gradle, we do not need to rely on any specific IDE/text editor (looking at you Eclipse)
    to do some of the most crucial tasks of our project.
- Additionally, it allows us to set up automated compilation, testing, and formatting as
    demonstrated in this repo.
- It uses a specific directory structure which seems to be well liked by the
    Java dev community. This structure separates test code from app code and within
    this separation it separates code based on language.

## What's in this repo?

- This repo uses Gradle in combination with Github Actions to run checks (compilation, tests,
    formatting) automatically on each pull request opened to master.

## Getting Started

1. Clone the repo:
    ```git clone https://github.com/rynoV/gradle-test```
2. Run `./gradlew` if you're on Mac/*nix, or `gradlew` if you're on Windows. This
    will set up Gradle so that you can run tasks.
3. Follow our workflow until the step where you rebase. At this point, run `git push`
    while still on the local feature branch. This should open a remote branch and
    push to that. You can then go to the repo and open a pull request.
4. After a pull request is opened, `gradle check` will be run on the Github Server
    and the result will be displayed on the pull request page. We can then review the
    code and merge the PR with master.
