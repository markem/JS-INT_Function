# JS-INT_Function
A Javascript int function

This is a simple Javascript INT function.  It doesn't need any calls to any other set of functions and only uses the Math, parseInt, and parseFloat operations/functions.  Enjoy!

This function (like many of my other functions are copyrighted but at the same time it is being released under a different license.  I have been releasing under the GNU license but decided (after reading through the MIT license) to use it instead.  Still, for the record, let me state publicly that this function can be used anywhere and anytime you feel like using it without any recourse by me for any kind of recompensation.  It would be nice if you put a blurb in your code that this was created by me - but you don't have to do so.  Or if you found it very useful if you would donate a dollar to me at sim_sales@sim1.us in PayPal.  But you DO NOT have to do that either if you don't want to do so.  It is just a suggestion - not a commandment.

What this function does:

It allows you to send over one or two arguments.  The firs argument is the variable that contains the number you want to use INT on.  The second OPTIONAL argument is how many places behind the decimal place you want it to keep.  Thus, the normal INT function simply calls parseInt() and let's Javascript do its normal thing.  BUT!  If you want the old way of doing INT (ie: 0.5 is added on to the number before truncating it) then call the function with TWO arguments.  The first is still the variable name but the second is (againn) how many places behind the decimal point you want to keep.  So if you just want to keep the integer part - you can call it with "(<variable>,0)" and it will just keep the whole number part.  If you send something like "(<variable>,2)" then two places behind the period will be kept.

How does it do this?

Javascript is really bad about not maintaining accuracy.  If you don't believe this try adding 0.01 on to the number zero.  It should go something like this: 0, 0.01, 0.02, 0.03, 0.04, 0.49999999.  That is really unacceptible to many businesses.  So you need a routine that will ensure that when Javascript mucks up - it can be corrected.  Thus - the INT function was born.  Does this mean it will ALWAYS be accurate?  No.  It does not.  There is no way for me to know what the outcome of some equation is supposed to be.  So what if A * B = C but C is something like 1.040000000000006?  (I actually had something like this happen.)  You can't tell, from looking at it, if it is supposed to be 1.04 or 1.05 because the equation that created the whacko number can't guarantee what the end product is.  So all you can do is to do an INT function on it and see if it comes out as 1.04 (which it will with this function).  I have seen Javascript also say that A * B = 436 when it really was 435.999999999991.  Again, this routine will restore that to 436.

Unlike the Math.floor() function which always makes the number the next whole number down from where it is (so that 436.00000006 becomes just 436) and unlike the Math.ceil() function which raises the number to the next number (so you would get 437), the int() function is trying to apply tried and true math principles to the number (ie: 0-4 rounds down and 5-9 rounds up).

I hope you like this function.  Enjoy!
