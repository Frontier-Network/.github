# Contributing to Frontier-Network

✨ Thanks for contributing to **Frontier-Network**! ✨

As a contributor, here are the guidelines we would like you to follow:

- [How can I contribute?](#how-can-i-contribute)
- [Respecting the workflow](#how-can-i-contribute)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Working with our repositories](#working-with-our-repositories)

We also recommend that you read [How to Contribute to Open Source](https://opensource.guide/how-to-contribute).

## How can I contribute?

You can help by:

- Improve documentation
- [Providing feedback on issues](#using-the-issue-tracker)
- Submitting a Pull Request for bug fixes or new features

### Using the issue tracker

The issue tracker is the channel for [bug reports](#bug-report), [features requests](#feature-request), and [submitting Pull Requests](#submitting-a-pull-request).

Before opening an Issue or a Pull Request, please use the [GitHub issue search](https://github.com/issues?utf8=%E2%9C%93&q=user:Frontier-Network) to make sure the bug or feature request hasn't been already reported or fixed.

Always create issues with the information requested in the [bug report guidelines](#bug-report).
Help us make it easier to resolve problems by adding relevant information.

Participating in the discussion is a great opportunity to get involved and influence our roadmap.

#### Bug report

A good bug report should provide enough information to avoid doubt or future questions.
Please try to be as detailed as possible in your report.

#### Feature request

Feature requests are welcome, but take a moment to find out whether your idea fits with the scope and aims of the project.
It's up to you to make a strong case for the merits of this feature to convince project developers to allocate time to it.
Please provide as much detail and context as possible.

## Respecting the workflow

It is important to understand and respect the **workflows** in place which may be different for each repository.
When we mention **workflows**, think of the soft human processes and the [automation](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions) that reduces repetition.

Any action that undermines the workflow can dilute the overall [idempotency](https://en.wikipedia.org/wiki/Idempotence#Computer_science_meaning) and subsequent reliability of our solutions, this usually leads to [unpredictable behavior](https://en.wikipedia.org/wiki/Chaos_theory), loss of reliability, and additional overheads of time and money.

If you have privilleged access to approve changes or take hard actions _(i.e. automation changes, repo settings, PR close/merge, etc.)_ where you may have a lack of comprehensive understanding in a specific circumstance; we ask that you be mindful that a small change, no matter how minor it may seem, can cause a large impact.
In these instances, if you have any doubt, seek guidance from subject matter experts.

## Submitting a Pull Request

Good Pull Requests, whether patches, improvements, or new features, are a fantastic help.
They should remain focused in scope and avoid containing unrelated commits.

**Please ask first** before embarking on any significant Pull Requests (e.g. implementing features, refactoring code), otherwise you risk spending a lot of time working on something that the project's maintainers might not want to merge into the project.

If you have never created a Pull Request before, welcome 🎉 😄.
[Here is a great tutorial](https://opensource.guide/how-to-contribute/#opening-a-pull-request) on how to send one :)

**Tips**:
- For ambitious tasks, open a Pull Request as soon as possible with the `[WIP]` prefix in the title, in order to get feedback and help from the community
- [Allow maintainers to make changes to your Pull Request branch](https://help.github.com/articles/allowing-changes-to-a-pull-request-branch-created-from-a-fork)
  This way, we can rebase it and make some minor changes if necessary
  All changes we make will be done in new commit, and we'll ask for your approval before merging them

## Working with our repositories

### Source code

To ensure consistency and quality throughout the source code, all code modifications must have:
- No [linting](#lint) errors
- [Valid commit message(s)](#commit-messages)
- Documentation for new features
- Updated documentation for modified features

### Documentation

To ensure consistency and quality, all documentation modifications must:
- Refer to brand in [bold](https://help.github.com/articles/basic-writing-and-formatting-syntax/#styling-text) with proper capitalization, i.e. **GitHub**, **Frontier-Network**
- Prefer [tables](https://help.github.com/articles/organizing-information-with-tables) over [lists](https://help.github.com/articles/basic-writing-and-formatting-syntax/#lists) when listing key values, i.e. List of options with their description
- Use [links](https://help.github.com/articles/basic-writing-and-formatting-syntax/#links) when you are referring to:
  - a **Frontier-Network** concept described somewhere else in the documentation, i.e. How to [contribute](CONTRIBUTING.md)
  - a third-party product/brand/service, i.e. Integrate with [GitHub](https://github.com)
  - an external concept or feature, i.e. Create a [GitHub release](https://help.github.com/articles/creating-releases)
- Use the [single backtick `code` quoting](https://help.github.com/articles/basic-writing-and-formatting-syntax/#quoting-code) for:
  - commands inside sentences, i.e. the `flux` command
  - programming language keywords, i.e. `function`, `async`, `String`
- Use the [triple backtick `code` formatting](https://help.github.com/articles/creating-and-highlighting-code-blocks) for:
  - code examples
  - configuration examples
  - sequence of command lines

### Commit messages

We have very precise rules over how our git commit messages can be formatted.  This leads to **more
readable messages** that are easy to follow when looking through the **project history**.  We also use the git commit messages to **generate changelogs**.

#### Atomic commits

If possible, make [atomic commits](https://en.wikipedia.org/wiki/Atomic_commit), which means:
- a commit should contain exactly one self-contained functional change
- a functional change should be contained in exactly one commit
- a commit should not create an inconsistent state (such as test errors, linting errors, partial fix, feature without documentation, etc.)

A complex feature can be broken down into multiple commits as long as each one maintains a consistent state and consists of a self-contained change.

#### Commit message format

Follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#specification) specification when writing commit messages.


**In summary:**
Each commit message consists of a **header**, and optionally a **body** & a **footer**.
The mandatory header has a special format that includes a **type**, a **subject**, and an optional **scope**:

```commit
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

An exclamation mark (!) must be added after the scope to indicate a **BREAKING CHANGE**.

The **footer** can contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages).

##### Type

The type must be one of the following:

| Type         | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| **chore**    | Any non-functional changes (i.e. documentation CI config, formatting, and external dependencies)            |
| **feat**     | A new feature                                                                                               |
| **fix**      | Any change, patch, or bugfix to an existing feature                                                         |

##### Subject

A casual observer must be able to understand what the change will achieve by reading at the subject.
Well written commit messages are vitally important for saving time, good record keeping, and avoiding misinformation.

The subject contains succinct description of the change without referring to previous behavior:

- stay within the soft 50/72 character limit in your commit header, use the commit body for extended descriptions while ensuring the header represents a summary of the entire change
- use the [imperative](https://git.kernel.org/pub/scm/git/git.git/tree/Documentation/SubmittingPatches?h=v2.36.1#n181), present tense: "change", not "changed", nor "changes"
- avoid capital letters
- avoid punctuation other than commas and those required to meet the specification
- avoid unnecessary context clues

##### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change.

##### Footer

The footer should contain any information about **Breaking Changes** and is also the place to reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.
The rest of the commit message is then used for this.

##### Examples

The following are a series of good examples:

```commit
feat: add pencil
```

```commit
fix(pencil): stop graphite breaking when too much pressure applied
```

```commit
feat(pencil): add options

This allows users to configure the pencil
```

```commit
feat(pencil/options): add graphiteWidth

The width of graphite can be configured in options

Fix #42
```

```commit
feat(pencil/options)!: remove graphiteWidth

BREAKING CHANGE: the graphiteWidth option has been removed

The default graphite width of 10mm is always used for performance reasons
```

Now, let's look at a **bad** example and the reasons it would not be acceptable:

```commit
chore (EraserTip/fix,attempt 2) Fixed the pencilcase by adding the new redTip Eraser to the Pencil and removing the glue like the last time!!
```

- `chore` is not appropriate type when adding/removing a feature, this example would likely be a `feat`
- as the header format is incorrect, any automation relying on it will fail
- the scope is used incorrectly, a scope cannot be used unless it was not added in a prior commit; additionally, unrelated strings `/fix` and `attempt 2` are not contextually relevant
- uppercase characters are used which can lead to inconsistent reporting or searching for changes, they are not required for communicating context
- past and future tense are used, imperative tense should be used which commicates what the commit **will** do if applied
- the word `fix` is used in some form other than for describing the type, and the phrase `fixed the pencilcase`, these are redundancies in linguistic expression; similar to "black darkness" or "burning fire"
- grammatical articles such as `the`, `a`, and `our`, including needless puntuation (`!!`) add no context, needlessly increasing the header length beyond the soft limit
- a casual observer cannot contextualise `new`, `some`, or `like the last time`, avoid references to prior/future state, this may waste time looking through surrounding commits to build an understanding of the change

We could correct this example to something similar to this:

```commit
feat(pencil/tip)!: add red tip, remove glue

BREAKING CHANGE: the glue will no longer hold the tip to the shaft

Users working in zero-gravity may experience involuntary decoupling of the pencil hardware
```

In the corrected example, these changes were made to produce a **good** example:

- we assume a sub-scope of `pencil`, specifically for changes to the `tip`, by nesting it in the scope as `pencil/tip`
  - this is permitted if a prior commit added the `tip` feature to the `pencil` scope, i.e. `feat(pencil): add tip`
- an exclamation mark (`!`) is added immediately before the colon (`:`) to indicate this is a breaking change
- a breaking change notice explains how the change will break prior use-cases
- unnecessary context, grammatical fillers, and needless punctuation were removed resulting in a consise message without loosing the important context
- as the automation can now read the commit message, the users of this feature will be correctly informed through changelog generation and the major version number increasing on release

## Working with our repositories

### Lint

Our repositories use [MegaLinter](https://megalinter.github.io/latest/) for linting and formatting and [pre-commit](https://pre-commit.com/) for validation.

### Versioning

We follow [semver](https://semver.org/) when versioning our artifacts, this should be automated as a result of following the [commit message format](#commit-message-format) using [release-please](https://github.com/googleapis/release-please).

### Pre-commit

Installing [pre-commit](https://pre-commit.com/) (see [docs](https://pre-commit.com/#install)) enables you to validate your changes before committing. This can help prevent linter issues in the pipeline and save some time during the review process.

### Merging and releasing

- Changes by humans are always manually reviewed by another human in the order they are submitted.
- If your Pull Request complies with the contributing standards in this document, and the change is accepted, it will be merged into the `main` branch.
