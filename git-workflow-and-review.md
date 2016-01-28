# Git Workflow & Code Review

## Master vs. Feature Branches

The `master` branch is considered production-ready in the sense that it
represents a clean, tested and reviewed version of the software. The
history of this branch must never be rewritten. The overall development
workflow is as follows:

1. Developer `X` wants to work on something
2. He/she creates a new branch off `master` for this work, e.g. via `git
   checkout -b x/this-and-that [master]`
3. He/she does the work and frequently commits to `x/this-and-that`
4. Whenever he/she considers the branch ready,
   [it is rebased against the latest `master`](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History):
   `git rebase -i master`. Among other things, this allows to
  * split commits up into small, ideally atomic commits (only changing
    one aspect at a time)
  * squash commits together
  * reorder commits so the development is easy to follow
  * improve commit messages (see [Commit Messages](#commit-messages)
  * get the branch ready for conflict-free merging into `master`
  * test whether the changes still work on top of the latest `master`
5. Steps 3 and 4 can be repeated as many times as needed; intermediate
   versions of the branch can be pushed to the main repository to get early
   feedback
6. Once the branch is ready for review, it is pushed to the repo and a
   merge request against `master` is submitted
7. Once the pull review is accepted through code review (see below),
   *and only then*, it is merged into `master` by the either the reviewer
   or the owner of the branch
9. The branch `x/this-and-that` may exist a little longer but can
   eventually be removed

### Code Review

Code review is performed on every pull/merge request. It is performed in
the way of commenting on the commit diffs included in the merge request
and on the merge request itself. Code review must be performed by a
different developer than the one submitting the merge request and may
comment aspects like these:

* Commit messages (see below)
* Coding style
* Inconsistencies (in naming, coding style and use of data structures
  and functions)
* Potential issues
* Code duplication

It is okay to comment on every single diff in a merge request if there
are remarks to be made.

If the reviewer considers the branch ready for merging, the reviewer
comments on the merge request with something like a `+1` or `Reviewed
and approved`. He or she then approves the merge request either in a
Terminal or via a UI like GitHub or GitLab.

### Commit Messages

It is strongly recommended to follow the [Git commit message guidelines
documented here](http://chris.beams.io/posts/git-commit/) for commit
messages.
