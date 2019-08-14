# code-climate-orb

Commands for uploading code coverage to Code Climate.

## Usage

#### What happens when I push a commit?

The Orb CI/CD pipeline begins! Your Orb will go through the `lint-pack_validate_publish-dev` workflow. The code will first be linted, then passed to the "pack" job which will take your multiple partial yaml files and condense them into a single Orb.yml file, lastly, if specified within the `config.yml`, and defined integration tests will also be ran.

Based on the branch you push to, the workflow will automatically create a development version of your orb for any branch except for "Master" which will create a production release which will be automatically incremented.

### Writing your orb
This orb provides a basic directory/file structure for a decomposed orb (where commands, jobs, examples, and executors each live in their own YAML file). Create each of your commands, jobs, examples, and executors within the requisite folders in the `src` directory.

Following are some resources to help you build and test your orb:

- [Tips for writing your first orb](https://circleci.com/blog/tips-for-writing-your-first-orb/)
- [How to make an easy and valuable open source contribution with CircleCI orbs](https://circleci.com/blog/how-to-make-an-easy-and-valuable-open-source-contribution-with-circleci-orbs/)
- Creating automated build, test, and deploy workflows for orbs: [part 1](https://circleci.com/blog/creating-automated-build-test-and-deploy-workflows-for-orbs/), [part 2](https://circleci.com/blog/creating-automated-build-test-and-deploy-workflows-for-orbs-part-2/)
