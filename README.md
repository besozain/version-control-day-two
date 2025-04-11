# version control day two

● To delete a remote branch
 git push origin :branch_name like test or dev
● To delete a local branch
 git branch -d branch_name like test or dev

Annotated tags vs Lightweight Tags
A lightweight tag is very much like a branch that doesn’t change — it’s just a pointer to a specific commit.
Annotated tags, however, are stored as full objects in the Git database. They’re checksummed; contain the tagger name, email, and date; have a tagging message; and can be signed and verified with GNU Privacy Guard (GPG). It’s generally recommended that you create annotated tags so you can have all this information; but if you want a temporary tag or for some reason don’t want to keep the other information, lightweight tags are available too.



When to use Rebase??
To Keep a Clean and Linear History:
Rebase is helpful when you want your commit history to be straightforward and without unnecessary merge commits.

When You Want to Avoid Merge Commits:
If you're working on a feature branch and you want to incorporate changes from the main branch without creating merge commits, rebase keeps the history neat.

To Update Your Feature Branch with the Latest Changes from main:
If the main branch has been updated with new commits, rebase can update your feature branch with these changes, making sure your work is built on top of the latest code.

To Clean Up Your Commit History Before Merging:
Before merging your feature branch into the main branch, rebase can help you organize, squash, or reorder your commits, ensuring a cleaner and more understandable history.

To Fix Small Issues in Commit History (Edit Commits):
If you need to make small corrections to earlier commits, like changing a commit message or modifying the content of a commit, rebase gives you the flexibility to adjust past commits.

When Working on Feature Branches Alone:
When you're the only person working on a feature branch, rebase can help keep your branch up to date with the latest changes from the main branch, and prevent issues later when you merge back into the main branch.


How to list tags? 
Listing the existing tags in Git is straightforward. Just type git tag (with optional -l or --list):
$ git tag
v1.0
v2.0
This command lists the tags in alphabetical order; the order in which they are displayed has no real importance.


How to delete tag locally and remotely?
# delete local tag '12345'
git tag -d 12345
# delete remote tag '12345' (eg, GitHub version too)
git push origin :refs/tags/12345
# alternative approach
git push --delete origin tagName
git tag -d tagName

