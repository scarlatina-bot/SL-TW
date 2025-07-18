// Interactive Object Script for Second Life
// This script responds to user touch events by changing the object's color
// and sending a friendly message in the local chat.

// Author: [Your Name]
// Date: 2025-07-18
// License: MIT (or your choice)

default
{
    state_entry()
    {
        llSay(0, "Interactive Object Initialized. Touch me!");
    }

    touch_start(integer total_number)
    {
        // Generate a random color vector (RGB)
        vector randomColor = <llFrand(1.0), llFrand(1.0), llFrand(1.0)>;
        
        // Apply the random color to all faces of the object
        llSetColor(randomColor, ALL_SIDES);
        
        // Notify users in local chat
        llSay(0, "Hey there! I just changed my color for you.");
    }
}
