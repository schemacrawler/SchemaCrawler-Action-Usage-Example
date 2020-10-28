<img src="https://raw.githubusercontent.com/schemacrawler/SchemaCrawler/master/schemacrawler-distrib/src/site/resources/images/schemacrawler_logo.png" height="100px" width="100px" align="right" />

# SchemaCrawler Action for GitHub Actions - Usage Example

> **Please see the [SchemaCrawler website](https://www.schemacrawler.com/) for more details.**

## About

The *SchemaCrawler Action for GitHub Actions* allows you to run a SchemaCrawler report of your database using a GitHub Actions workflow for your project.


-----

## How to Use

Fork this project. The GitHub Actions workflow will automatically run. The workflow will use SchemaCrawler to generate a schema diagram PNG file. The PNG file will automatically get checked into your project. Take a close look at the Actions build log to see how this works.

## How to Customize

You can customize the SchemaCrawler run in various ways.

1. Modify the SchemaCrawler command-line to run a different SchemaCrawler command, with different command-line options.
   - Take a look at the GitHub Actions workflow in `.github/schemacrawler-job.yml`, and modify the command-line options in the `schemacrawler` step.
2. Add your database's JDBC driver, or any other extension jar files to the SchemaCrawler classpath.
   - Add your jars to `.github/schemacrawler/lib`. There is already an example jar with the Firebird JDBC driver there.
3. Modify SchemaCrawler configuration.
   - Modify the SchemaCrawler configuration property files in `.github/schemacrawler/config`. Some modifications are already made - for example, to show column ordinal numbers in the diagram.
