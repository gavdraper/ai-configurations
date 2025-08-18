# Coding Behaviors

As a coding agent you should think thoughly, it's ok for this to take some time. Avoid unnecessary repetition.

ALWAYS exhibit the following behaviors
* write clean code that complies with SOLID principles
* write tests at the most appropriate level adhering where possible to the test pyramid
* NEVER remove a failing test just because you can't make it pass
* if you need to delete a test because its no longer relevant ask me first and tell me the reasons
* create classes in their own files
* If you get stuck please let me know, give me options and ask for my thoughts
* before bringing in a new library ask me first
* If asked to commit ALWAYS do it on a feature branch
* code should be self documenting, comments should not be required

After completing a task ALWAYS do the following
* run a clean build and check it passes, if it doesn't then fix any issues
* run ALL tests not just the ones close to the changes, check they ALL pass and fix any that fail
* run a security review of changes - then fix issues
* run a code review on changes - then fix issues
* run a review of the changes against the task and make sure they cover everything asked

The following tools are available for you to use
* GitHub CLI - Viewing/Creating Issues, Creating PRs
* Curl - Quick testing of endpoints, these are throw away tests and should be created as automated tests in our testing framework where they are something worth keeping

# Workflow
When asked to start a new piece of work that has no plan, if the work has more than a couple of steps then ALWAUS ask if I'd like the initiate the plan workflow, if I say yes then do the following

* Create a unique file in the folder agent-tmp
* In that file breakdown all the steps of your plan and store them as a checklist
* Ask me if I'm happy with the plan

Once the plan is complete if I ask you to start work or continue take the first incomplete item in the plan and start work.

Once the work is complete and meets all the requirements of the Behavior section above you may mark the step as complete in the markdown file and stop. 
