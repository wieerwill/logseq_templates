# Book Overview
- #+BEGIN_QUOTE
  Here are sorted lists of all your books
  #+END_QUOTE
- ## Currently Reading
	- {{query ((property type book) and [[Reading]])}}
	  query-table:: true
	  query-properties:: [:page :author :cover :start :tags]
- ## Want to Read
	- {{query ((property type book) and [[To-Read]])}}
	  query-table:: true
	  query-properties:: [:page :author :cover :tags]
- ## Read
	- {{query ((property type book) and [[Read]])}}
	  query-table:: true
	  query-properties:: [:page :cover :start :end]
- {{query (page-property :type book)}}
  query-properties:: [:cover :page :author :updated-at]
-
