issue-prompt
============

A Git hook which prompts for an issue number when committing, then adds it to your message. Never neglect to reference your project's issues again... at least not on accident! Many project management tools (including GitHub) utilize Git hooks to perform operations on issues when they are referenced in commit messages. This simple client-side git hook makes sure you don't forget to include issue numbers in your commits.

## How to use

After you install the hook (see below), you will be prompted for an issue number everytime you make a commit `git commit`. After you provide the number, you will be asked if this commit resolves the referenced issue. If it does not resolve the issue, issue-prompt will append "Issue #{issue number}" on a new line in your commit message. If your commit does resolve the issue, "Fixes #{issue number}" will be appended to your message.

If you do not want your commit to reference an issue, simply press enter when you are prompted for an issue number. Your commit message will remain unchanged.

## Installation

1. Clone this repository `git clone git@github.com:chasingmaxwell/issue-prompt.git`.
2. Create a symlink to the commit-msg file inside your project's .git/hooks directory `ln -s issue-prompt/commit-msg /path/to/your/project/.git/hooks/commit-msg`.
