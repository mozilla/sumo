# Mozilla Sumo

This repository is used to track anything related to the platform that powers SuMo and any other projects the team might be working on.

## Engineering Board

We are working mostly with projects. A project signifies the team's focus for a period of time. Usually there are one or two active projects at a time.
A project is defined as a standalone chunk of work for a specific property. Recent examples of projects were the redesign of the SUMO site, integrating Firefox Accounts etc.

As a rule of thumb, a project is defined as work that requires more than one tasks to be completed and takes more than 3 working days. Anything that doesn't fall in the project category
is a standalone issue. In most of the cases, these issues are bugs.

_The board will only display either standalone issues or the issues of the active project(s) in order to avoid clutter._

### GitHub Milestones

We are using milestones to better organize the work that a project needs in order to be completed. A milestone is a concrete chunk of work and each project can have more than one milestones.

An example of the above structure is:

- Site Redesign - project
  - create designs - Milestone1
    - GH issue
    - GH issue
    - GH issue
  - implement designs - Milestone2
    - GH issue
    - GH issue
    - GH issue

Not active rojects may have a placeholder milestone in the form of a Inbox if there are already existing issues in board. This is purely for organization reasons.

### Labels

Labels are used to easily distinguish cards that have them attached. We should keep them to the minimum in order for the cards that hold them to easily stand out.
We are not using priority labels. Priority is determined by the position of a card in the board.

We have the following labels to highlight an issue:

- Bug:
  Something is not working properly.

  _Any issue that has the bug label should also be assigned to the KTLO GitHub milestone regardless of the severity of the bug._

- Pr-welcome:
  Tasks friendly to new contributors. These tasks are only closed when they are done.

- Comms:
  Tasks that need to be performed by project stakeholders and are related to any communication that needs to take place before a release.

### Columns

#### Triage/Parking Lot column

This column only holds standalone issues and projects that are not currently active.

#### Backlog column

Hold the tasks of individual _active_ milestone(s) or standalone tickets that will be worked on within a few weeks.

#### Comms/Dependencies/Blocked column

This column holds all the tasks that require collaboration with project stakeholders or there are blocked for any reason.

#### In Progress column

Specific tasks that are actively worked on by the team.

A card is moved to the next column only when a PR is opened.

#### Review column

Anything that waits for a review. An issue is moved to the next column only when merged.

#### Merged column

Merged in the default branch but pending deployment to a testing environment.

#### QA column

Everything that is already released to the testing environment and is ready to go under QA.

If an issue passes the QA process, it will be moved to the next column.
Otherwise it will be moved back to the `In Progress` column.

If new issues are opened from the QA processes, they should go under the `Next Items` column without anyone assigned.

#### Ready for Release column

Acts as a parking lot. This column is suitable for anything that successfully passed QA but is not yet released to production.

An effort should be put to keep this column short.

#### Done column

That's all!

## Release notes

After each release, we are posting a summary of what happened in [Discourse](https://discourse.mozilla.org/c/sumo/22).
