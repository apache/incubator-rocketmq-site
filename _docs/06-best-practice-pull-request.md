---
title: "How to manage Pull Request"
permalink: /docs/pull-request/
modified: 2016-12-24T15:01:43-04:00
---

This page guides you through Git setup and contribution process.

{% include toc %}

# Git setup for Contributors
First of all, fork github’s [apache/rocketmq](https://github.com/apache/rocketmq) to your own account on github and clone it as follows,

    git clone https://github.com/<your_github_name>/rocketmq.git

Cloning this locally will set up `origin` to point to your remote fork on github as the default remote.
Now you can create your pull requests.

You will need to update a local master sometimes (to merge to your development branches).
For this, you have to add remote for RocketMQ mirror as follows,

    git remote add apache https://github.com/apache/rocketmq.git
    
and update your local master via `git fetch` followed by `git rebase`, for instance:

    git fetch apache master
    git rebase apache/master
    
# Do some work on the branch

    git checkout -b ROCKETMQ-xxxx # create a branch 
    git commit -a -m "doing some work"
    git push origin ROCKETMQ-xxxx # notice pushing to **origin** not **apache**
    
Once you are ready to commit to the apache remote you can merge and push them directly, otherwise always create a PR.

# How to create a PR (committers)

Push your branch to Github:

    git checkout ROCKETMQ-xxxx
    git push origin ROCKETMQ-xxxx
    
1. Go to your ROCKETMQ-xxxx branch on Github. Since you forked it from Github's apache/rocketmq. By default all PR will go to apache/master.

2. Click the green "Compare, review, and create pull request" button. You can edit the `to` and `from` for the PR if it isn't correct. The "base fork" should be apache/rocketmq unless you are collaborating with one of the committers on the list. The "base" will be master. Don't submit a PR to any other branches unless permitted by branch owner. The "head fork" will be your forked repo and the "compare" will be your ROCKETMQ-xxxx branch.
3. Click the "Create pull request" button and name the request "ROCKETMQ-xxxx" all caps. This will connect the comments of the PR to the mailing list and issue comments.
4. From now on the PR lives on github's apache/rocketmq. You can use the commenting UI there.
5. If you are looking for a review or wanting to share with someone else please write a note in the comments and don't worry about automated merging of your PR -- you will have to do that later. The PR is tied to your branch so you can respond to comments, make fixes, and commit them from your local repo. They will appear on the PR page and be mirrored to Github issue and the mailing list.
6. When you are satisfied and want to push it to Apache's remote repo, you can merge this PR.

# How to create a PR (contributors)
Before you create a pull request, make sure
1. A corresponding [Github issue](https://github.com/apache/rocketmq/issues) is created and has a clear problem description.
2. Make sure you follow [Coding Guidelines](/docs/code-guidelines/).
3. You have unit tests for everything you are about to commit. All pull requests are automatically tested at [Travis CI](https://travis-ci.org/github/apache/rocketmq) on AMD64 and ARM64 CPU architectures.

For information about creating pull requests, please check [GitHub PR docs](https://help.github.com/articles/creating-a-pull-request/).

Pull requests are made to `apache/rocketmq` repository on Github. 
In the Github UI you should pick the develop branch as target of the PR. <br />
You pull request will be reviewed and commented by committers, and issues can be discussed. When all reviewers are positive on the pull request, it will be merged.

# Check List for a PR

Each pull request should follow the [checklist](https://github.com/apache/rocketmq/blob/master/.github/PULL_REQUEST_TEMPLATE.md) to help us incorporate your contribution quickly and easily.

Remember use `- [x]` mark an item finished in the check list and there is a [demo pull request](https://github.com/apache/rocketmq/pull/152) can be your reference. 

# Merging a PR (yours or contributors)
Start with reading [GitHub PR merging locally](https://help.github.com/articles/checking-out-pull-requests-locally/). Remember that pull requests are equivalent to a remote github branch with potentially a multitude of commits. In this case it is recommended to squash remote commit history to have one commit per issue, rather than merging in a multitude of contributor's commits. In order to do that, as well as to close the PR at the same time, it is recommended to use squash commits.
Merging pull requests are equivalent to a "pull" of a contributor's branch:

    git checkout master      # switch to local master branch
    git pull apache master   # fast-forward to current remote HEAD
    git pull --squash https://github.com/cuser/rocketmq.git ROCKETMQ-xxxx  # merge to master
    
`--squash` ensures all PR history is squashed into single commit, and allows committer to use his/her own message. Please refer to git help for merge or pull for more information about `--squash` option. In this example we assume that the contributor's Github handle is "cuser" and the PR branch name is "ROCKETMQ-xxxx". Next, resolve all conflicts, or ask a contributor to rebase on top of master, if PR went out of sync.

If you are ready to merge your own (committer's) PR you only need to merge (not pull), since you have a local copy that you've been working on. This is the branch that you used to create the PR.

    git checkout master      # switch to local master branch
    git pull apache master   # fast-forward to current remote HEAD
    git merge --squash ROCKETMQ-xxxx
    
Please run regular patch checks, build with tests enabled, and change CHANGELOG whenever needed.
If all requirements are met, you can commit the squashed request using:

    git commit --author="contributor_name <contributor_email>" -a -m "ROCKETMQ-XXXX description closes apache/rocketmq#ZZ"
    
ROCKETMQ-XXXX is all capitalized and ZZ is the pull request number on apache/rocketmq repository. Including "closes apache/rocketmq#ZZ" will close the PR automatically. More information can be found here [GitHub PR closing docs.](https://help.github.com/articles/closing-issues-via-commit-messages/).
Next, push to apache:

    git push apache master
    
(this will require Apache handle credentials).
The PR, once pushed, will get mirrored to github. To update your github version push there too:

    git push origin master
    
Note on squashing: Since squash discards remote branch history, repeated PRs from the same remote branch are difficult to be merged. The workflow implies that every new PR starts with a new rebased branch. This is more important for contributors to know, rather than for committers, because if new PR is not mergeable, github would warn at the start. Please watch for dupe PRs (based on same source branches).

# Closing a PR without committing (for committers)
When we want to reject a PR (close without committing), we can just issue an empty commit on master's HEAD without merging the PR:

    git commit --allow-empty -m "ROCKETMQ-XXXX closes apache/rocketmq#ZZ *Won't fix*"
    git push apache master
    
that should close PR ZZ on github mirror without merging and any code modifications in the master repository.



