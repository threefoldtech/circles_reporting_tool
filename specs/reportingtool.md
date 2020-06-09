# reporting tool

- user logs in using 3bot connect
- user can configure: github name (because can be different compared to 3bot connect), stored in local config mgr
- fetch all stories, tasks, projects, epics ... into local stor (redis backend?) 
    - re-fetch every 5 min
- in generic wiki site:
  - create a wiki page per story, task, ...
  - use templates (cjinja2 on crystal) per type 
  - in each page make links to people, story (if subitem), to epic, ...
- create some predefined 

## components used

crystal tools
- publishing tools (make site per user and a generic one)
- jsng wizards for certain tooling for the user (phase 2)


## real wizard (phase 2)

- use jsng (jumpscale next gen)?
- allow user to see a grid with for himself or other user
    - stories 
    - issues
    - story checklist items
    - github issues (sorted per type, story, ...)
- allow user to filter based on
    - deadline (see what is overdue)
    - time since start (e.g. story open for +2 weeks)
    - type of issue
    - source of issue/story/...
