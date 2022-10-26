# One2Many Field Operation

<pre>
<b>(0, 0,  { values })</b> link to a new record that needs to be created with the given values dictionary
<b>(1, ID, { values })</b> update the linked record with id = ID (write *values* on it)
<b>(2, ID)</b>             remove and delete the linked record with id = ID (calls unlink on ID, that will delete the object completely, and the link to it as well)
<b>(3, ID)</b>             cut the link to the linked record with id = ID (delete the relationship between the two objects but does not delete the target object itself)
<b>(4, ID)</b>             link to existing record with id = ID (adds a relationship)
<b>(4, [ID])</b>           link to existing record with id = ID (adds a relationship)
<b>(5)</b>                 unlink all (like using (3,ID) for all linked records)
<b>(6, 0, [IDs])</b>       replace the list of linked IDs (like using (5) then (4,ID) for each ID in the list of IDs)
<b>(5, 0, 0)</b>           unlink all
</pre>
