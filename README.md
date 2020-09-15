# sumo-project

This repository is used to track anything related to the platform that powers SUMO

## Engineering Board

Short description of the workflow and of the columns in the board.

### GitHub Milestones

Mostly used for grouping for long standing projects such as KTLO work.

### Labels

Labels are used to easily distinguish cards that have them attached. We should keep them to the minimum in order for the cards that hold them to easily stand out.
We are not using priority labels. Priority is determined by the position of a card in the board.

There are two kind of labels:

- Labels that correspond to a specific project (kitsune vs respond). There are as many labels as the projects that the team is working on. Available labels are:
  - Kitsune
  - Respond
  - Community Portal
- Labels used to highlight an issue. This is a short list of labels.

  - Bug:
    Something is not working properly.

    _Any issue that has the bug label should also be assigned to the KTLO GitHub milestone regardless of the severity of the bug._

  - Pr-welcome:
    Tasks friendly to new contributors. These tasks are only closed when they are done.

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

#### Blocked column

Well this column is used for blocked items.

A description why this issue is blocked should exist in the card.

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

## SUMO PM & Design Board

TBD
