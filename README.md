# Mozilla Sumo & Community

This repository is used to track anything related to the platform that powers SuMo and any other proejcts the team might be working on.

## Engineering Board

Short description of the current workflow of the team.

We are working mostly with projects. A project signifies the team's focus for a period of time. Usually we are are working on a single project per property at a time.
A project is defined as a standalone chunk of work for a specific property. Recent examples of projects were the redesign of the SUMO site, integrating Firefox Accounts etc.

Work outside of projects usually falls under the Keep the Lights On category (KTLO).

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

The only execption to the above is the KTLO milestone which is used as a group selector for all relevant tasks that fall under that.

### Labels

Labels are used to easily distinguish cards that have them attached. We should keep them to the minimum in order for the cards that hold them to easily stand out.
We are not using priority labels. Priority is determined by the position of a card in the board.

There are two kind of labels:

- Labels that correspond to a specific property. There should be as many labels as the properties that the team is working on + 1. Available labels are:

  - Kitsune
  - Other
    Catch-all identifier for non-sumo work. If there is a need it can break down to specific projects.

- Labels used to highlight an issue. This is a short list of labels.

  - Bug:
    Something is not working properly.

    _Any issue that has the bug label should also be assigned to the KTLO GitHub milestone regardless of the severity of the bug._

  - Pr-welcome:
    Tasks friendly to new contributors. These tasks are only closed when they are done.

  - Comms:
    Tasks that need to be performed by project stakeholders and are related to any communication that needs to take place before a release.

### Columns

#### Triage column

Catch-all column. Anything filed in this repository goes to this column.
Triage should happen regularly and the column should not have many cards.
An exception to this are the cards that hold the `pr-welcome` label.

A card from here either moves to the `Backlog`, `Next Items` or it is closed.

**A card can be closed, even if it is valid, if it is not going to be worked on in more than six months**.

#### Backlog column

A backlog of tasks that will be worked in the next three months.
Ideally meta-issues should be used here.

#### Next items column

Smaller prioritized backlog with cards that will be worked on in the two upcoming weeks. Should be sparsely populated and frequently updated.

If there is an urgent bug, it can be moved directly here.

#### Comms/Dependencies/Blocked column

This column holds all the tasks that require collaboration with project stakeholders or there are blocked for any reason.

#### In Progress column

Anything that it's actively worked on.
Ideally nobody should own more that three cards in this column.

A card is moved to the next column only when a PR is opened.

#### Review column

Anything that waits for a review. An issue is moved to the next column **only** when merged and deployed to a testing environment.

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
