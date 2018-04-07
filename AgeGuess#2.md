#
# Created by: Aayman Shameem
# Created on: Apr 06, 2018
#
# This code will guess the age of the user through the input
#

# the input of the user
userInput = int( input() )

# if the input is greater than 16, then it's too big
if userInput > 16:
	print( "Too big, wanna try again?" )
pass

# show negative if less than zero
if userInput < 16:
	print( "Too small, wanna try again?" )
pass


# show 0 if equal to zero
if userInput == 16:
	print( "CORRECT!!! The End." )
pass


exit( input( "Enter" ) )
