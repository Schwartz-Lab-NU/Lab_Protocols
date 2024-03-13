# Simple Neurite Tracing Tutorial
Written by Trung 07/23

**Requirement**
SNT (simple neurite tracing) in fiji

## Steps
### Stiching
- Open the image
- Run Deinterleaver -> 3 Channels
- Get rid of the blue transmitted channel
- Adjust B and C
- Image -> Merge Channels -> Create composite (Ignore source LUT)
- Image -> 8 bit for color 3D stiching
- Save each image as TIFF.
- Do the same thing for all other images
- Put a square in the overlapping areas on each image.
- Plugins -> Stiching -> Pairwise stiching
- Registration channel -> Only channel 1.
- Diffusion method: Diffusion blending.
- Put the scaling back by looking Image -> Properties for the original pictures. Then go
to the new stich image. Put pixel size correctly, set the unit correctly to  , and voxel
size 0.5. **DO DIS BEFORE ANY TRACING**
- Splitt the stiched image into components. Save the images into
filenamecellname_cell.tiff and filenamecellname_chat.tiff

### Tracing
- Press SNT button
- Press SNT
- Choose the correct image.
- Leave the reconstruct blank.
- XY view is enough.
- Select Gray LUT for the image so that the color of path does not overlap.
- Open Path Manager window.
- Start double clicking on the trace. Y for each point to save that segment. N to redo thesegments.. F to finish.
- Branching: select Path (1). Hit Option on Mac (alt on Windows) for branching. Start
clicking on points and Y to save. Everything should be under path 1. What branches of
what is not really important. Getting everything filled is more crucial.
- Hit J to select the closest branch to start forking.

- Save as you go along.
- Save Traces As -> .traces, and Path Manager -> Analyze -> Sketonize, save
skeleton under filenamecellname_skell.tiff
- .swc format for standardization at the end.
### Filling
- Select all paths at once in Path Manager
- Fill
- Start with default (Should be gud enough)
- Store to store the fill
- Reload the correct fill
- Export As... -> Binary Mask.
- Save the binary mask as filenamecellname_mask.tiff
- Process -> Image calculator. Multiply the original image with the mask and scale
- B&C correctly for pretty image.
### Analysis
- Select all paths. Save as filenamecellname.swc
- Call CHAT_analyzer_GUI from MATLAB Command Windows.
- Load Chat image -> Choose the CHAT image.
- Load dendrite image -> Choose the the dendrite image (the one color image).
- Boxes per line mess around.
- Auto detect peaks -> Compute surface. Find the two CHAT bands im the 3D surface.
- Select box. Click on the graph to define the CHAT bands. Get the two smaller peaks.The higher peak is the soma.
- Save surfaces. Save as filenamecellname_CHATsurface.MAT.
- Run RGCMorphologyAnalyzer from MATLAB Command Window.
- File -> Load skeleton image (the _skell.tiff). Load surfaces and Load
swc.

- Draw surface on skeleton.
Select Lower surfcae to CHAT On, Upper surface to chat_off, choose Unwarp. Onceit's done, it redraws as unwrap.
- Analyze -> Stratification profile and Arbor properties.
- When you're done Save analyze data file as
filenamecellname_arborData.mat
- Checke Bistratified for cells that are bistratified so it does analyses for upper and lower
