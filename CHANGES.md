This file serves as a brief outline of my thoughts/findings throughout this little project.

1. `public static string ToCommaSepatatedList(string[] items, string quote)`
    - Identified the spelling mistake in the variable name. Changed 'ToCommaSepatatedList' to 'ToCommaSeparatedList'.
2. `StringBuilder qry = new StringBuilder(string.Format("{0}{1}{0}", quote, items[0]));`
    - If items has a length of 0 we run into `IndexOutOfRangeException`. To fix this, we check this condition before accessing the array.
    - In my revised code this is fixed by accessing the `items` array inside of the for loop. Since `i` is initialised as 0, if `items` is empty it will not be accessed.
3. The original code has two sections in which items were added, once using the StringBuilder constructor, and once using the `Append` method. I changed this so the only time that items are added are inside of the for loop. 
   - Results in simpler code since both lines are two lines of code were reduced to one.
4. `qry` variable is not descriptive. Changed to `delimitedString` as I believe is it a better representation of what the variable represents.