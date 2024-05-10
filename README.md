# <img src="https://raw.githubusercontent.com/schemacrawler/SchemaCrawler/main/schemacrawler-website/src/site/resources/images/schemacrawler_logo.png" height="100px" width="100px" valign="middle"/> SchemaCrawler Action for GitHub Actions - Usage Example

> **Note**: Please see the [SchemaCrawler website](https://www.schemacrawler.com/) for more details.

## About

The *SchemaCrawler Action for GitHub Actions* allows you to run a SchemaCrawler report of your database using a GitHub Actions workflow for your project.


-----

## How to Use

Fork this project. The GitHub Actions workflows will automatically run. One workflow will use SchemaCrawler to generate a schema diagram PNG file, and make it available as an artifact of the job run. The other workflow will run SchemaCrawler lint. The workflow will fail on lint errors, but the lint report will be available as an artifact of the job run.

> **SchemaCrawler can also be used in GitLab jobs. For an example, please see [sualeh/schemacrawler-action-usage-example](https://gitlab.com/sualeh/schemacrawler-action-usage-example).**

## How to Customize

You can customize the SchemaCrawler workflows in various ways.

1. Modify the SchemaCrawler command-line to run a different SchemaCrawler command, with different command-line options.  
Take a look at the GitHub Actions workflows in `.github/workflows`, and modify the command-line options in the `schemacrawler` step.
2. Add your database's JDBC driver, or any other extension jar files to the SchemaCrawler classpath.  
Add your jars to `.github/schemacrawler/lib`. There is already an example jar with the Firebird JDBC driver there.
3. Modify SchemaCrawler configuration.  
Modify the SchemaCrawler configuration files in `.github/schemacrawler/config`. Some modifications are already made - for example, to show column ordinal numbers in the diagram.

## Further Reading

Also take a look at the following article for ideas on how you could use the SchemaCrawler Action
- [Generate Database Diagrams With GitHub Actions Workflows](https://dev.to/sualeh/generate-database-diagrams-with-github-actions-workflows-4l96)
- [Lint Your Database Schema With GitHub Actions Workflows](https://dev.to/sualeh/lint-your-database-schema-with-github-actions-workflows-57cg)

