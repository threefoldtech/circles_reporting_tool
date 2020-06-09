# reporting tool

purpose: all people to see their issues, stories, tickets in circles.threefold.me and github.

- user logs in using 3bot connect
- github name stored in e.g. circles.threefold.me profile
- if not there yet, fetch all stories, tasks, projects, epics ... into memory (nice model)
    - re-fetch every 5 min
- generate wiki pages 
  - create a wiki page per story, task, ...
  - use templates (cjinja2 on crystal) per type 
  - in each page make links to people, story (if subitem), to epic, ...
  - create some predefined pages per user (smartly chosen criteria, github & circles)
    - stories, links to subitems
    - issues
    - ...

## components used

crystal tools
- publishing tools (generate wikis)
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
