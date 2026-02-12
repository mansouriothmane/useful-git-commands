# Useful git commands

#### Reset last commit

```bash
git reset HEAD~1  
```
Use case: we already commited something locally, but the remote branch was deleted.

#### Add changes to specific commit

In this example, it is the second-to-last commit.
The first approach is Interactive Rebase. The other one, which I find better is to do a `fixup`:

First, stage and commit changes as a fixup:

```bash
git add <files>
git commit --fixup=HEAD~1
```

Then, rebase with autosquash:

```bash
git rebase -i --autosquash HEAD~3
```


