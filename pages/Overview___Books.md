# Book Overview
- #+BEGIN_QUOTE
  Here are sorted lists of all your books
  #+END_QUOTE
- ## Currently Reading
	- {{query (and [[Books]] [[Reading]])}}
	  query-table:: true
	  query-properties:: [:page :author :cover :start :tags]
- ## Want to Read
	- {{query (and [[Books]] [[To-Read]])}}
	  query-table:: true
	  query-properties:: [:page :author :cover :tags]
- ## Read
	- {{query (and [[Books]] [[Read]])}}
	  query-table:: true
	  query-properties:: [:page :cover :start :end]
- {{query (page-property :type [[Book]])}}
  query-properties:: [:cover :page :author :updated-at]
-
