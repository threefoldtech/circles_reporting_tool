# reporting tool

purpose: all people to see their issues, stories, tickets in circles.threefold.me and github.

- user logs in using 3bot connect
- github name stored in e.g. circles.threefold.me profile
- if not there yet, fetch all stories, tasks, projects, epics ... into memory (nice model)
    - re-fetch every 5 min
- generate wiki pages 
  - create a wiki page per story, task, ...
  - use templates (jinja) per type 
  - in each page make links to people, story (if subitem), to epic, ... on circles tool
  - create a page per user on which to show
    - stories, links to subitems
    - issues
    - funnel items (is a story in project starting with FUNNEL_)
    - ...

## components used

- jsng
- publishing tools (to show the wiki)

## circles have a predefined format

each circle used is a copy from a template

### team

- name starts with TEAM_
- https://circles.threefold.me/project/despiegk-template_circle_team

### funnel

- name starts with FUNNEL_
- is to track business opportunities
- see [funnel](funnel.md)

### project

- name starts with PROJECT_


### archive

- name starts with ARCHIVE_
- do not use in exports


## smart usage of circles tool

### different type of objects


 to be completed
