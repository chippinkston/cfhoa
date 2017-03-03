#CFML Coding Standards.
This application uses the FW/1 framework and associated DI/1 and AOP/1 libraries.

* All `cfc` files must be written in cfscript.
* Views can use `cfml` tags.
  * The following tags are allowed in views:
     * `cfoutput`
     * `cfif / cfelse`
     * `cfswitch`
     * `cfloop`
     * `cfset`\*
  * Anything else needs to be in a `controller` or `service` and in cfscript.
  
\* `cfset` can only be used to assist in simplifying complex statements into easier to test cases, or to manage flow in looping constructs.

Example:
```
<cfset canEdit =	user.isAdmin() || 
			user.isAccountHolder() || 
			user.isAccountAdmin()
>
<cfif canEdit>
	<button>Edit</button>
</cfif>
``` 