# Civic Tech Field Guide Directory

> The Civic Tech Field Guide is the world's biggest collection of projects using tech for the common good.

## General

We use the [Code for All](https://codeforall.org/) `#civic-tech-field-guide` Slack channel for project coordination and discussion.
If you want to help out, you should [join the Slack community](https://slack.codeforall.org/) and the channel and say hi.

All contributions are welcome. If you found a bug and want to provide a fix, fork the repo, work on the fix and [create a PR](https://docs.github.com/en/github-ae@latest/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork).

If you wish to contribute a feature or provide general support, contact [Matt Stempeck](https://github.com/mstem), among many things, the Curator of the project, to fill you in on the project's priorities.
[Benjamin Munyoki](https://github.com/bmunyoki) is the project's main developer; you should ask him to review your work.

## Get started

The Directory is based on Laravel 7.
If you are not familiar with it, first [check out their docs](https://laravel.com/docs/7.x/) to understand the basic concepts and the requirements to run it locally.

The source of truth is an [Airtable database](https://airtable.com/shrfxjImCdCNw9p5U/tblELFP9tGX07UZDo).
When listing projects or filtering them, instead of directly querying Airtable, we use a regularly synced SQL database.
The sync is one-directional; the SQL database is read-only.

### Setting up the site locally

1. Clone the forked repo (`git clone`) and run the Composer install (`composer install`) command.
2. Create a `.env` file based (`cp .env.example .env`) on the `.env.example` and fill out the details.
3. Generate a key (`php artisan key:generate`) then run the migration (`php artisan migrate`) command.

At this point, the Directory should be functional, although there won't be any project in the database.

#### Importing the database

If you don't yet have access to the Airtable database, you can import the SQL [database dump](https://codeforall.slack.com/archives/C02S6CXE1KR/p1649871812694029) shared in the Slack channel.

If you have access to the Airtable database and provided the `AIRTABLE_KEY` and `AIRTABLE_BASE` values in the `.env` file, run the `php artisan sync:tables` command.

## Other ways to contribute

You don't have to be a developer to contribute. Check out our [Contribute page](https://civictech.guide/contribute/) to find details about all the ways you can help us.

## License

This guide and directory are free to use, re-use, adapt, and modify for non-commercial purposes as long as you link back with attribution, and share alike with the same license.
