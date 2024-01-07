- # Time Box
  template: time_box
  template-including-parent: false
	- ## Meta
	  type:: timebox
	  tags:: timebox
	  icon:: 📅
	  date:: <% today %>
	- # Brain Dump
	  	#+BEGIN_NOTE
	  	Take everything that’s in your brain that you need to get done and jotted down as quickly as you possibly can. Don’t think about it. Just write them down
	  	#+END_NOTE
    	- 1. Blah Blah
    	  1. Blah Blah
	- # Top Priorities #.kanban
	   #+BEGIN_NOTE
	   List out your Tasks Categorized by Task
	   #+END_NOTE
	- ## 🔴 High {{renderer :todomaster}}
		- [#A] Low Priority Task
	- ## 🟡 Normal {{renderer :todomaster}}
		- [#B] Normal Priority Task
	- ## 🟢 Low {{renderer :todomaster}}
		- [#C] High Priority Task
		- # Morning Box #.kanban
		- query-table: true
		  #+BEGIN_NOTE
		  Build your Morning Plan
		  #+END_NOTE
			- ## 7 AM
			- ## 8 AM
			- ## 9 AM
			- ## 10 AM
			- ## 11 AM
		- # Afternoon Box #.kanban
		  #+BEGIN_NOTE
		  Build your Afternoon Plan
		  #+END_NOTE
			- ## 12 PM
			- ## 1 PM
			- ## 2 PM
			- ## 3 PM
			- ## 4 PM
		- # Evening Box #.kanban
		  #+BEGIN_NOTE
		  Build your Evening Plan
		  #+END_NOTE
			- ## 5 PM
			- ## 6 PM
			- ## 7 PM
			- ## 8 PM
			- ## 9 PM