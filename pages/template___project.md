- # Project
  template:: project
  template-including-parent:: true
	- ## Meta
	  Type:: [/[project]]
	  Tags:: project
	  icon: 📂
	  title:: 
	  Status:: [/[Idea]] [/[Planned]] [/[Active]] [/[Completed]]
	  Team:: 
	  Lead:: 
	  Goals:: 
	  Start:: 
	  End::  
	  areas::
	  priority::
	- ## Objective/Goal
		- 
	- ## Scope
		- 
	- ## Project Kickoff Checklist
		- 
	- ## Tasklist
		- TODO Setup project page
	- ## Tasks
		- {{query (and <% current page %> (task LATER))}}
	- ## Resources
	- ## Notes
	- ### Project Meta
		- DOING [#B] #project <% current page %>
		- query-table:: false
#+BEGIN_QUERY
{:title [:h2 "Related Tasks"]
 :query [:find (pull ?b [*])
		 :in $ ?query-page
		 :where
		 [?p :block/name ?query-page]
		 [?b :block/marker ?marker]
		 [?b :block/refs ?p]
		 [?ref :block/name "project"]
		 (not [?b :block/refs ?ref])
		 [(contains? #{"TODO" "DOING" "NOW" "LATER" "WAITING"} ?marker)]]
 :inputs [:query-page]
 :result-transform (fn [result]
					 (sort-by (fn [b]
								(get b :block/priority "Z")) result))
 :breadcrumb-show? false
 :group-by-page? false
 :collapsed? false
}
#+END_QUERY
#+BEGIN_QUERY
{:title [:h2 "Checklist"]
 :query [:find (pull ?b [*])
		 :in $ ?tag
		 :where
		 [?b :block/marker ?marker]
		 [(contains? #{"TODO"} ?marker)]
		 (page-ref ?b ?tag)
		 [?ref :block/name "project"]
		 (not [?b :block/refs ?ref])]
 :inputs [:query-page]
 :result-transform (fn [result]
					 (sort-by (fn [b]
								(get b :block/priority "Z")) result))
 :breadcrumb-show? true
 :table-view? false
}
#+END_QUERY
#+BEGIN_QUERY
{:title [:h2 "Completed Related Tasks"]
 :query [:find (pull ?b [*])
		 :in $ ?query-page
		 :where
		 [?p :block/name ?query-page]
		 [?b :block/marker "DONE"]
		 [?b :block/refs ?p]
		 [?ref :block/name "project"]
		 (not [?b :block/refs ?ref])		 
		 ]
 :inputs [:query-page]
 :result-transform (fn [result]
					 (sort-by (fn [b]
								(get b :block/priority "Z")) result))
 :breadcrumb-show? false
 :group-by-page? false
 :collapsed? false
}
#+END_QUERY