Splunk Commands and what they do:

1) Stats Count - Counts all of the number of events in your search
Ex: index=security sourcetype=firewall
    | stats count by src_ip

2) Fields - Fields command is used to add or remove mentioned fields from the search results. To remove the field, minus sign ( - ) is used before the fieldname and plus ( + ) is used before the fields which we want to display.
   Syntax: | fields <field_name1>  <field_name2>
   Ex: | fields + HostName - EventID

3) Search - This command is used to search for the raw text while using the chaining command |
   Syntax: | search  <search_keyword>
   Ex:  search "Powershell"

4) Dedup - Dedup is the command used to remove duplicate fields from the search results. We often get the results with various fields getting the same results. These commands remove the duplicates to show the unique values.
   Syntax: | dedup <fieldname>
   Ex: | dedup EventID\

5) Rename - It allows us to change the name of the field in the search results. It is useful in a scenario when the field name is generic or log, or it needs to be updated in the output.
   Syntax: | rename  <fieldname>
   Ex: | rename User as Employees
