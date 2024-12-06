# Tcl Subtle Division-by-Zero Bug

This repository demonstrates a subtle division-by-zero error in a Tcl procedure. The error is not immediately apparent because a conditional statement checks for the numerator being zero. However, it fails to handle cases where the numerator is not zero but the denominator is not a valid number.  This can cause unexpected crashes in the script.

## Bug Description
The procedure `badproc` checks if the input parameter 'a' is equal to 0, if so it returns 0. It fails to handle the case where 'a' is not 0 and 'b' is not a numeric value.  This leads to an error when division is attempted on a non-numeric value.

## Bug Solution
The improved procedure `goodproc` adds error handling using the 'string is double' command to check if both inputs are numbers.  This prevents the division-by-zero error and also handles any cases where the inputs are not numbers. 