# Spirogen
A web application for creating geometric visualizations and animations, with the ability to react to music

 <img width="2416" alt="Spirogen Demo Shot 1" src="https://user-images.githubusercontent.com/44735056/221964739-b73315e9-b615-4291-bb79-c4510f9fe58a.png">


## Disclaimer
This is a very fresh project that I am actively working on. Some features aren't finished yet, and many others are yet to come. There is currently no mobile UI, and likely will never be, given the complexity, desktop is recommended (chrome seems to have the best rendering performance).

[The Spirogen app is live! Check it out here](https://www.spirogen.net/) (on a computer, not mobile, chrome is recommended)

## Basics:

- The 'Layers' section in the top left shows patterns, and the controls that show below modify the selected pattern
- Layer Controls: macro parameters that affect the pattern globally (usually less interesting/necessary)
- Pattern Controls: parameters that affect how shapes are multiplied, transformed, rotated, etc. in each 'branch'
  - example: with a branch length of 20 (20 individual shapes per branch) and an x shift of 20, each shape in a given branch will be shifted 1px (20/20) from the previous
- Shape Controls: type & form the shape that is repeated in the pattern
- Color Schemes: shows a list of all color schemes in the project. To link a given color scheme to a given pattern, click the gradient swatch on the Layer entry, and click on the scheme you want (should be flashing in link-mode)
- Color Scheme Controls: swatches and parameters for the color scheme
  - length controls how many stops total are generated in the gradient. If you want the gradient to be completed fully in a pattern, 'length' should match 'branch length' of the pattern
  - shift controls where in the gradient the pattern starts
- MODULATORS (the cool part!)
  - 3 types: oscillators, automation, & audio
  - To link a modulator to a parameter, click the |-> looking icon on the modulator entry, and once you see control parameters highlighted, click and drag on one until the link-indicator bar range looks good
  - Oscillator modulators are always running (for now)
  - Timeline modulators are linked to tracks in the timeline (at the bottom of the page) and will not make anything move unless playing (space bar or button at top)
  - Any time you click a modulator, the relevant controls will appear below the modulator list sections
- Saving/Exporting
  - Exporting to video has not been implemented, but you can save & load .spirongen files using the buttons at the top right

MORE DETAILED INSTRUCTIONS WILL BE POSTED SOON!

## What's in the works:
- [x] Tooltips for buttons
- [x] Epillepsy warning
- [x] Welcome modal with demo projects to check out
- [x] Wave shape performance optimizations
- [x] Modulation link editing interface
- [x] Renamable tracks, layers, color schemes, and modulators
- [x] Floor/Threshold parameter for audio modulators
- [x] Audio waveforms & spectrums as shapes
- [x] Grid pattern type [still improving]
- [ ] Shapers (apply a function to parameters to determine how they change over time/space)
- [ ] Demos with audio/automation
- [ ] Instructions/walkthroug
- [ ] Info/Help system (panel that shows info about whatever is hovered over, similar to Ableton Live & Bitwig Studio)
- [ ] Export project as video
- [ ] Login
- [ ] Save projects to your account in the cloud
- [ ] Undo/redo
- [ ] Waveform shape from audio data
- [ ] Macros (create controls to assign to an arbitrary number of controls, with an arbitrary affect amount)
- [ ] Background color (not just black background)
- [ ] Community section (peruse projects that others have created)
- [ ] Timeline navigation ergonomics options & improvements
- [ ] Switch to OpenGL (svg rendering is the performance bottoleneck, and it often gives visibly aliased results)
- [ ] Reorder color swatches, or add new ones wherever
- [ ] Global speed control (just oscillators, or possibly timeline content as well)
- [ ] Duplicate layers, color schemes, modulators, etc, for modification from a common point
- [ ] Hue slider for color scheme
- [ ] Allow other modulator parameters as modulation targets

## Keyboard Shortcuts:
- <kbd>f</kbd>: toggle full-screen view
- <kbd>space</kbd>: pause/play
- <kbd>t</kbd>: open/close timeline
- <kbd>ctrl/⌘</kbd> + <kbd>s</kbd>: save svg file of the pattern, exactly as it is at that second
- <kbd>ctrl/⌘</kbd> + <kbd>shift</kbd> + <kbd>←</kbd>: save the project as a `.spirogen` file
- <kbd>esc</kbd>
  - if in fullscreen, exit fullscreen
  - else if in linking-mode, exit linking mode
  - else if the timeline section is open, close it

I am keeping the source-code private for the time-being, as I am still considering whether there is business potential for this project, but, for anyone curious, the stack is Svelte, TypeScript, SASS, Node, & AWS. 

*Note: You may have been directed here from a reference to the legacy version of this project (tkinter Python application). That version has been moved [here](https://github.com/TheDitis/SpiroGen-Legacy)*

