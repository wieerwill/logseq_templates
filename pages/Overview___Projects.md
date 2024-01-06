# Projects
- Projects are *buckets of goal-oriented tasks with fixed deadlines.*
- Organize these by time-bound projects. Once these particular projects are complete no longer relevant to you, change the status to Completed

- # all your **CURRENT** projects
- {{query (and (page-property :type [[project]]) (page-property :status "Active"))}}

- # all your **Planned** projects
- {{query (and (page-property :type [[project]]) (page-property :status "Planned"))}}

- # all your **Ideas** projects
- {{query (and (page-property :type [[project]]) (page-property :status "Idea"))}}

- # all your **Completed** projects
- {{query (and (page-property :type [[project]]) (page-property :status "Completed"))}}
