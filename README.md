# Cline Dev Cheatsheet

- Naming items is really important and using those names in every prompt is important. If you call something a participant in one place and a user in another prompt, it will not be able to reconcile the two.
- Keeping a running development_queue.md seems to work, however it suffers from the same truncation issues as your code files, so make sure Cline isn't wiping out chunks of it.
- This is my system prompt:

```
You are **Cline**, a visionary full-stack developer, UI/UX designer, and product strategist. Your expertise spans from ecosystem mapping and MVP creation to complex system architecture and project management. You excel at breaking down complex projects into manageable components, rapidly developing **Minimum Viable Products (MVPs)**, and planning for their integration into a cohesive ecosystem.

Always refer to the document_map.md in the cline_docs folder for important documentation.

As eash task is completed make sure you update the development_queue.md to reflect what's been done and what should happen next.

Remember to ALWAYS INCLUDE THE FULL CODE when updating a file. Do not create placeholders like "everything else remains unchanged".
```

- Build and Deploy early and often so you're not spending hours fixing things after 80% of your dev is done.
- Remind Cline to go back to your database schema when adding new features so it gets the naming of properties correct, otherwise it assumes names that may not be right
- As you soon as you hit 300 lines, refactor
- Restarting VSCode every once in a while seems to help if you're stuck in a loop
- "review the documentation" seems to force it to review what's not working, like an invalid import.
- Paste a link to a documentation URL for something that's it struggling with
- Remember the modules and frameworks that have been added, and don't let it run off in 5 ways for the same thing in 5 places. Had some grief with icons where there were three different icon frameworks used in three different places.
- Remember what components have already been created, don't let it create a component that already exists just because it assumes it doesn't
- "Try again - you're deleting a lot of code" sometimes helps with code truncation.
- I've had the most success with django and nextjs (independently)
- Try to monitor what's been forgotten in standard development workflow. If Cline added a new field to the database then was the database migration done? If a new module was used was the package.json updated?
