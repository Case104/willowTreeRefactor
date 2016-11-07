##API

:art:
Fetch already returns a promise, so the code is a little redundant.
Although 200 is the most popular, it is better to use response.ok, which returns true if the response code is 200-299, in this case I recommend printing the error to the console.
Updating syntax to keep it uniform.

(https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
(https://developer.mozilla.org/en-US/docs/Web/API/Response/ok)

##Data Transforms

###getFirstName // getLastName

:art:
The current design of this method assumes that the second name is the last name. New method breaks names that end in '2', but I believe that it is better practice and that the database should be updated with better constraints.
Coding style should be consistent, and in this case it should be a function.

:goat:
Splitting the string yields better performance than Regex.

(https://jsperf.com/query-str-parsing-regex-vs-split/2)

###shuffleList
:art:
Currently mutates the passed in list.
Uses hard to follow variable names.
Returns with one less object.


###filterByName
:tada:
Currently only matches once full name is entered.


###sortObjectListByProp
:art:
Should use slice(0) instead of slice(1) for copying.

(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

###sortByLastName
:art: :fire: :goat:
Method currently sorts by first name z-a.


