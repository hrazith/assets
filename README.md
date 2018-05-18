assets
======

Visual design assets for wirefarming and prototyping

GS UITK
Queryfield
Overview
Queryfield combines features of a data filter with a search and lookup
field. This particular component allows the user to query a search result
with any and all combinations of free-form text along with a set of
predetermined filter terms.
How It works
When the field is in focus, a list of predetermined filter terms are displayed
underneath. On selecting a term, the term is ‘pill-ified’ at the search field
and a new list of pertinent comparison operators are displayed for options.
The user may cap off with a free-form search term or chain additional filter
terms and operators.
The component can be configured to accept any number of filter terms
and operators. Users may choose to combine a free-form query term with
either a strict (= or ≠) or relational operators( <,>, etc.) to make
comparisons against filter terms.
Eg: Name equals Jones, Age less than 40.
The Queryfield can interact with other components such as the grid and
the chart.
Anatomy of a Query Field
<annotated image of QF here>
Try Me!
.
Usage
The level steps for Queryfield integration are as follows:
1. Choose dimensions (categories) and create config
2. Transform data into Queryfield format
3. Give config to Queryfield
4. Update dimensionValues based on filter and current predicate
Expected data format
{
dimensionName: 'Name', // the dimension
value: 'Dan Smith', // the actual value to use
displayText: 'Dan Smith' //the value to display
}
In the code example we show how the data and dimension values can be
transformed into one format for the queryfield.
Interactions
Build a Predicate
• Search for and select the dimension
• Search for and select the operator
• Search for and select the value
Select a Predicate.
• Simply use the arrow keys, ← → to perform the selection and
remove with Backspace
Conjunctions.
• All predicates that are in the same dimension should use
the OR conjunction.
<image here>
• All predicates that are in different dimensions should use
the AND conjunction.
<image here>
DOs
• Work with the designer to make sure the number of options do
not overwhelm the users or break the UI layout
DONTs
• Don’t create too many pills. When all the pills are used it cannot
be longer than the width of queryfield. Limit it to 5 or fewer pills.
<image here>
• Don’t create too many operators. Limit the number of operators to
5 - 6 where possible. Be aware of the amount of vertical real
estate it might take up.
API
Property Description Required Default Type
Enter something here Enter something here Data Data Data
onQueryChange Function that gets
called when...
False No-Op Function
Enter something here Enter something here Data Data Data
