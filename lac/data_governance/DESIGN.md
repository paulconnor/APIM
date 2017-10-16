There are 3 ways that the data can be securely accessed
1) Directly from the data base table using security-roles for each of the classification levels and then mapping these roles to authentication tokens
2) Via additional resources that filter and remove fields based on the logical data classifications provided
3) Via a new Function that traverses the data model and calls the required resource APIs using an Auth Token to filter out data as in  (2) above

TODO:
To make the data governance model completely dynamic, rules are required to fire off any updates to the data model and call the LAC API to create new resources, users, roles, tokens as required
