# Dugga-Doo-3D-Model
Dugga Doo, Dugga Doo, Dugga Dugga Dugga Doo

You may have seen my YouTube video where I spent a week animating a 3D model of Dugga Doo. Well, here are a few versions of that 3D model.

I then spent another week refining it only to then realize I had been working with an INACCURATE REFERENCE IMAGE THAT WHOLE TIME. IT WAS ONE OF THE FEW SCENES WHERE DUGGA DOO HAS A RETRACTED NECK AAAH. but I'm personally out of time and will wait for somebody else to make a pull request lol.

<br><br>

# 3D Model Summary

### Lower_Poly_Dugga
![Lower polygon count 3D model](https://github.com/DoctorWhoFan1234/Dugga-Doo-3D-Model/blob/main/lower_poly_dugga/preview_images/preview.gif)

This 3D model has 2,337 vertices and doesn't look too great if I'm being honest, but this was my first time remeshing, and these were the automatic results with very few modifications. Okay, I'd prefer if somebody else remesh the high poly version to replace this with a more accurate low poly version.

Anyway, this version has the fur as a solid mesh with no skin underneath, but this model is probably good enough and simple enough for realtime applications like game development and such. Also if you have a slow computer this one's probably best.

<br>

### Proper_Dugga_Doo
![High polygon count 3D model](https://github.com/DoctorWhoFan1234/Dugga-Doo-3D-Model/blob/main/proper_dugga_doo/preview_images/preview.gif)

This model has 63,467 vertices and was the raw version I sculpted. The Blender file also has a subdivision surface modifier enabled so that makes it closer to 240,000 vertices. It has a solid mesh fur variant, as well as a version where the user is expected to add the fur/hair themselves, whether it be simulated as hair particles, or added via a method like shell texturing for realtime application.

Here is the solid mesh fur variation, at 246,882 vertices:<br>
![High polygon count 3D model with solid mesh as fur](https://github.com/DoctorWhoFan1234/Dugga-Doo-3D-Model/blob/main/proper_dugga_doo/preview_images/mesh_fur.gif)

<br>

### Video_Dugga
![Rough video version of the 3D model](https://github.com/DoctorWhoFan1234/Dugga-Doo-3D-Model/blob/main/original_dugga/preview_images/preview.gif)

This was the first model I made, and the one I used for the video. It's quite rough, with its [insert number] vertices, it really doesn't match the official 3D model that well, and the head is an entirely separate object from the body, but it worked. Also I adjusted the mouth and eyes a bunch throughout the video so this version only truly matches the Dugga Doo found in the electric guitar segment.

To use this one you gotta simulate the hair. Not too sure why you'd want to use this one other than the fact the bigger eyes and 

<br>

Here's a comparison between the new "proper" version and the one I used for the video

![Comparison Between the new 3D Model and Original](https://github.com/DoctorWhoFan1234/Dugga-Doo-3D-Model/blob/main/proper_dugga_doo/preview_images/comparison.gif)

<br><br>

# Usage Instructions
The mesh is segmented between the body and the parts of the face, for ease of use. Every 3D model except Lower_Poly_Dugga has eyelids and an animation in the non-linear animator for blinking. The Blender `.blend` file contains inverse kinematic constraints on the legs for easier animation, but apparently that can't be exported so that's stuck only in the `.blend` file version of each 3D model.

Shape Keys were used for the mouth motions. They can be exported but I think I've heard other programs call them different things, so check for the equivalent to Blender's Shape Keys in whichever program you're using.

Hair simulation in the Blender versions have three particle systems: hair, body, and head/tail.<br>(The reason for head/tail is that hair simulation gets thinner in narrower parts of the mesh so adding more fur hides that fact)

<br><br>

# Detailed Blender Usage Instructions
To those unfamiliar with Blender, here are more specific instructions.

When you open the .blend file, you should be in the `Layout` tab. If not, then on the top of the screen, click the `Layout` tab. Slightly below the tab buttons and to the right, Blender should display a dropdown in the top left that says `Object Mode`. If the dropdown does not say this, then click the dropdown and change it to Object Mode. Now you can select any of the 3D objects.

To look around and navigate, you can use the middle click button on a mouse, or use two fingers on a touchpad. Alternatively, there's a little XYZ coordinate model in the top right. To zoom in/out, use the mouse scroll wheel, or on a touchpad separate/pull together your fingers. To focus on the selected object, press the `.` on the number pad. If your keyboard doesn't have a numberpad click the top left menu items `View` > `View Selected`

So, let's start things with adding a camera. press `shift+a` to add a new object (or use the `Add` button on the top left, but that's kinda slow). Now you can search for a camera, and then get that. If you got the wrong thing you can press `x` to delete it. Now that you have a camera, you can move it around through the use of the main Blender shortcuts: `g` (grab), `r` (rotate), and `s` (scale). To see what the camera sees, you can press 0 on the number pad, or if your keyboard doesn't have a number pad, you can click `View` > `Cameras` > `Active Camera`
(background images can be attached to the camera, and audio can be added via a `Speaker`, but I am too tired to explain how to do that part. Find an online tutorial if you're unfamiliar)

To move the mesh, you must select the bones. In the hierarchy on the top left, there are 2 armatures, or skeletons for the model, indicated by an icon that looks like a T-posing 3D model. One is the skeleton for the Dugga Doo mesh, and the other is a "target" for where the feet go, and where the toes and knees should point.<br>You must select both these skeletons (either through shift+click or shift+arrow_key, or ctrl+click), and now in the normal viewer window where you can see the mesh, you can move it around through the use of the Blender shortcuts: `g` (grab), `r` (rotate), and `s` (scale)

To make a keyframe, press the `i` button. Now it's saved this current position, rotation and scale as a keyframe in the timeline on the bottom of the screen. You can `g` (grab) and `s` (scale) the keyframes in the timeline, too, to retime the actions.<br>To make another keyframe, move the vertical blue bar to another frame in the timeline by clicking the number above it and drag it over to a frame later in the timeline. Now you can move things again and make another keyframe.<br>Or, to automatically have blender set the keyframe at the current position without you having to press the `i` button, click the circle next to the playback buttons on the timeline at the bottom of the screen. This enables Auto Keying (and the circle should turn red when enabled).

To expand/shrink the timeline, there are little numbers on the right hand side of the timeline in the bottom window. `Start` determines the frame in which the animation starts, and `End` determines the which frame is the last frame of the animation.

To give Dugga Doo a new pose, select the skeleton you wish to adjust (if you can't select it, you may not be in `Object Mode`, so check the top left!), and then once it's selected, click that dropdown in the top left that says `Object Mode` and change it to `Pose Mode`. Now you can use the `g` (grab), `r` (rotate), and `s` (scale) Blender shortcuts to move the bones of the body. To save a keyframe here, make sure you select the bone you want to save the keyframe of, and press `i` like before.

To reset the bones to Dugga Doo's original pose, select the bones and press `alt+g` to reset position, `alt+r` to reset rotation, and/or `alt+s` to reset scale. If you have the NVIDIA app then I'm sorry, but NVIDIA hates you and you'll have to go through the NVIDIA app and disable the game overlay in order to reset the pose.

To move the mouth, first make sure you're in `Object Mode` and select the mouth. In the bottom right properties window, you will see a green upside-down triangle button that says "Data" when you hover over it. Click that and you will see the Shape Keys area. There are 4 shape keys: `dugga` (mouth closed), `doo` (mouth noot-noot-ing), `oo` (mouth slight smaller, so the mouth doesn't ever stop moving), and finally `OOOOOOOO` (mouth extremely outstretched, to catch the 15th Doctor before he falls out the airlock in Space Babies)<br>To use these shape keys, you will see a number to the right of each pose and can click and drag to increase or shrink that number (or you can click and manually type the number). To keyframe this, hover the mouse over the number and press `i`

For more fine-grained control over the animation, look online into the `Dope Sheet` and `Graph Editor` and MAKE SURE YOU NOTICE THE SEARCH BAR IN THE TOP LEFT. HOW DID I NEVER SEE THAT BEFORE IT WAS AN ABSOLUTE LIFE SAVER. But anyway my instructions here assume you remain in the `Timeline` editor, so keep that in mind (the others, while allowing EXTREME PRECISION, don't let you set the `Start` and `End` frame number, nor enable/disable `Auto Keying` for some reason).

To simulate the hair/fur, click the mesh you wish to simulate the hair on, and the go to the Particles tab in the bottom right properties window, which has an icon that looks like four blue dots in the shape of a square. Okay I don't know how to describe this icon. Anyway, once you click on it you will see the hair particle systems. You can't simulate all of them at once, but you can select each hair system and then scroll down to the `Cache` submenu. Save the project first because sometimes the hair gets glitchy. Select the simulation length in terms of start frame and end frame and then press `Bake`. If it glitched out, you can mess with the quality settings perhaps, or you could just give up and not have it simulate at all: delete the bake and then scroll up a little and disable `Dynamics`. Do the same for the other two hair simulations.

For rendering and exporting, there really isn't too much to it. Make sure Blender uses your graphics card if you have one, use Cycles for hyperrealism (but EXTREMELY SLOW rendering) or EEVEE for faster but less accurate renders. Enable `Transparent` in the `Film` submenu of the rendering tab of the properties menu to make the background transparent, then you can overlay the animation on the background in the compositor (or export in a form with transparency; I recommend an exr set to DWAA (lossy) because I saw a YouTube video about that once). I am not describing this part in too much detail though, so find an online tutorial if necessary.

Alright that should be most of it. Good luck, everybody!