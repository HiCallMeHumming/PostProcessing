# Transitions for the Post-processing Stack

Collection of scripts that allow you to seamlessly transition between 2 PostProcessingProfiles based on time or distance

## What is supported:
* Seamless, fluid, smooth, awesome transitions
* Switch profiles over time
* Switch profiles over distannce
* Trigger zones to switch profiles
* All numeric (float / int) values in PP effects

## What is not yet supported
* Lerping booleans (we have the method, but it needs fine-tuning to be seamless)
* Lerping textures (no method yet)
* Color grading (too much work for the initial version and I hope to come up with a better coding solution)

I have not tested Unity versions < 5.6. I have not extensively tested the smoothness of every single transition

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


# Post-processing Stack

Need help ? Check out the [quick start guide](https://github.com/Unity-Technologies/PostProcessing/wiki) and [the official forums](https://forum.unity3d.com/forums/image-effects.96/) !

Found a bug ? Let us know and [post an issue](https://github.com/Unity-Technologies/PostProcessing/issues) !
