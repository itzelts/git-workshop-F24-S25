# T4SG Git Workshop (F24-S25) Activity

This activity consists of a series of small exercises to apply the concepts in the workshop slides in practice. In the activity, you will:

- add, commit, and commit changes to a copied version of the repository
- create new branches and practice merging, rebasing, and creating pull requests
- resolve merge conflicts
- revert and reset commits

Aside from copying and cloning the repository on to your machine, all the exercises below can be done independently. Feel free to skip questions if you're stuck or want to move on!

#### Exercise 1: Template and Clone the Repository

Creating a template of a repository is analagous to creating a copy of google slide or doc. It creates another remote repository that is independent from the original.

To create a template in the **_Code_** of the repository, navigate to the **_Use this template_** button in the right-hand corner. From there, you should check **Include all branches** and give the repository a descriptive name.

Again, make sure to check **Include all branches**. For the exercises below, you'll want access to all the branches from the original.

After filling in the fields,
click **_Create Repository_** to be re-directed to the new repository.

Now, to clone the repository, click on **_Code_**, and copy the url under HTTPS or
SSH. From there, in your terminal, run

```
git clone <git@github.com:USER-NAME/REPOSITORY-NAME.git>

# e.g cloning the original repository
git clone git@github.com:hcs-t4sg/git-workshop-F24-S25.git
```

After cloning, open the repo in you preferred code editor (i.e. VS Code), and in your terminal, enter the directory

```
# list files in current directory
ls

cd <repo_name>

# e.g.
cd git-workshop-F24-S25
```

#### Exercise 2: Create a Branch and Add a Feature

Create a new branch called _answers_ and switch to it.

Create a new file called `answers.md`, and take 3-5 minutes to answer the following
questions:

1. What is the difference between git and GitHub?
2. Why is version control important?
3. What is the command to view a branch's commit history?
4. What command lists all the branches in your local repository? Which one lists those in the remote?
5. To prevent specific files and folders from being commited to a repository, what should you do?

Write your answers in `answers.md` (the format is up to you). After you're finished,
make a commit and push your changes. Then, make a PR to merge into main.

Before merging the PR into main, navigate to the **_Files Changed_** tab, where you'll see files with lines highlighted in
green and red. Looking at the base branch as a baseline, green represents additions in the compare branch while red represents deletions.

Hover over a line of code and click the plus symbol. Add a sample comment. In PRs, collaborators can reference specific lines of code by making in-line comments.

Merge `answers` into main and navigate to the branches view of the repository. You'll see that `answers` is now marked as **_Merged_** and is now safe to delete.

#### Exercise 3: Merging Branches and Resolving Conflicts

There are two branches `mergeA` and `mergeB` each with markdown files labeled from 1 to 6.
Make a pull request with `mergeA` as the **_base_** branch and `mergeB` as the **_compare_** branch.
Upon comparing each branch, you will see that an automatic merge fails and that you will have to
manually resolve conflict files.

To resolve the conflicts flagged in the PR, merge `mergeB` into
`mergeA` (i.e. `mergeA` will become the merged version of the two) by either accepting the current change,
the incoming change, or both changes. Then, once you've resolved all conflicts and commited and push the merge
to the repository, complete the PR.

#### Exercise 4: Rebasing Branchings

Now, navigate to `rebaseA` and `rebaseB`. Both of these branches should look familiar,
being identical counterparts to the original versions of `mergeA` and `mergeB`. Like exercise 3,
integrate the changes from both branches such that `rebaseB` is combined into `rebaseA`. However, instead
of a merge, use a **_rebase_**.

#### Exercise 5: Squashing Commits

In the branch `squash`, you will see that the last three commits are fairly similar, each adding information
about a T4SG member named Jayden. Squash these three commits into a single commit titled
"added biography information for Jayden".

#### Exercise 6: Reverting Commits 
In `revert`, there were 5 commits made in consecutive order, each labeled from A-E. 
In a commit *l*, a message was added to `index.md` that reads: "This is a message from commit {l}".
Make a series of reverts such that the commit history becomes A-B-C-D-E-C'-D' with C' and D'
referring to commits C and D being reverted. Before executing the reverts, what do you expect `index.md` to
look like in D'? 

After making these reverts, use `git cherry-pick` to return the branch to a commit identical to that of E.

#### Exercise 7: Reset Commit History
There are two branches `reset-soft` and `reset-hard` that are based off `revert`. 
In each branch, perform a reset (soft on `reset-soft` and hard on `reset-hard`) 
to bring the commit history back to commit `C`. In `reset-soft` recover your changes 
to return the branch back to `E`. Unfortunately, once you have pushed changes after a 
hard reset, they cannot be recovered!

#### Exercise 8: Git Issues
As the last exercise of this workshop, open an issue on the main repository (not the fork)
and open an Issue with a few sentences. In the Issue, please feel free to either: 
- Introduce yourself 
- Talk about something you learned new at this workshop
- Feedback about how the workshop was run, content, etc. 
- Anything else! 

Thank you for attending!
