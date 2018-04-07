-----------------------------------------------------------------------------------------
-- Created by: Aayman Shameem
-- Created on: Apr 05, 2018
--
-- This code will make the age of the user depending on the input
-----------------------------------------------------------------------------------------

-- the question being asked
local titleText = display.newText( "How old are you?", display.contentCenterX, display.contentCenterY - 488, native.systemFont, 177 )

-- the place to input the age
local ageInput = native.newTextField( display.contentCenterX, display.contentCenterY - 177, 720, 277 )

-- the text to be replaced with the right or hints to the right
local answerText = display.newText( "The guess is: ", display.contentCenterX, display.contentCenterY + 430, native.systemFont, 177 )

-- the age button
local ageButton = display.newImageRect( "./assets/sprites/enterButton.png", 675, 277 )
ageButton.x = display.contentCenterX 
ageButton.y = display.contentCenterY + 177
ageButton.id = "the age checking button"

-- the button of age checking
local function theAgeButton( event )
	
	-- to make sure the string input turns into a number
	local realAge = tonumber(ageInput.text)

	-- if the number is higher than 16, it's too big
	if realAge > 16 then
	    answerText.text = "Guess is too big, try again."
	

	-- if number is lower than 16, it's too small
	elseif realAge < 16 then
		answerText.text = "Guess is too small, try again."
	

	-- if the number is 16, then the answer is right
	elseif realAge == 16 then 
		answerText.text = "CORRECT!!! Wanna go again?"
	

	-- if there is no value, then show "THERE MUST BE A NUMBER!!!"
	else answerText.text = "ERROR!!! THERE MUST BE A NUMBER!!!"
	end
end

ageButton:addEventListener( "touch", theAgeButton )
