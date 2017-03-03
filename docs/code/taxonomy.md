#Taxonomy
##Keys
* Primary Keys for each table must be `id`
* Foreign Keys must be `{{description}}_id`.
  * The description should be clear about the target table.  e.g. If we record a history for multiple items, do *NOT* name the fkey `history_id` - rather make it clear that is it `{{item}}_history_id`.
* Relationships need to be defined in the Database, and not just in the Application.
  * DBMS providing, FKey relationships should have a descriptive name to assist in clarifying the relationship.
  * FKey names must follow the convention of `FK_{{parent_table}}_{{child_table}}`.

##Dates
* Date fields must start with the word `date` followed by the type of date.  E.G.:
  * `dateCreated`
  * `dateUpdated`
  * `dateFounded`
  * `dateStart`
  * `dateEnd`
* Date fields must be timestamp fields.
* Dates must be based on UTC with zero (0) offset.
  * User accounts should specify their time zone.

##Booleans
* All fields that represent a boolean state must either start with:
  * `is{{fieldName}}` - to represent a singular state
  * `has{{fieldName}}` - to represent a potential plurality state