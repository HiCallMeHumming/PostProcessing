# Transitions for the Post-processing Stack

Collection of scripts that allow you to seamlessly transition between 2 PostProcessingProfiles based on time or distance.

# Updates

May 23, 2017 Update: We are using the stable branch (v1) of Unity-Technologies/PostProcessing
February 2, 2018 Update: The v2 branch of Unity-Technologies/PostProcessing now supports most of the operations done here, out of the box: https://github.com/Unity-Technologies/PostProcessing

This means that if you are using 2017.1+ you probably want to go there and consider this repo DEPRECATED

## What is supported:
* Seamless, fluid, smooth, awesome transitions
* Switch profiles over time
* Switch profiles over distannce
* Trigger zones to switch profiles
* All numeric (float / int) values in PP effects

## What is not yet supported
* Lerping booleans (we have the method, but it needs fine-tuning to be seamless)
* Lerping textures (no method yet)

If you don't care about the rest of the staff from PostProcessing, just grab the "Transitions" folder. I haven't changed anything else (nor do I plan to)

I have not tested Unity versions < 5.6. I have not extensively tested the smoothness of every single transition. Lmk if there's anything wrong.

## How to use - Time

1. Create 2 PostProcessingProfiles, we'll call them A and B.
*Hint: Try to use the same effects in both, but change the numeric values significantly to notice the effect!*
    1. Add a PostProcessingBehaviour to your camera
	  2. Assign profile A to it
2. Create an empty object and add a collider on it
    1. Use the collider to cover an area where you would like the to switch to B profile
    2. Set the collider as trigger
3. Add a TimePostProcessingTransition to the object
    1. Assign profile B as Future Profile
    2. Assign how long you want the transition to take under Config/Time for Transition
4. Click Play, move inside the trigger zone and watch the transition effect!
