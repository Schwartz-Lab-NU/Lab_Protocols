# Checklist before recording
The idea of this checklist is to go over the steps in multiclamp and symphony in order to record.

A detailed explanation on how to make the membrane tearing for CA, and seal and break the membrane for patch, is better done in person. 

0. Mark the mouse as deceased on AI
## Coordinates and condenser focus
1. Inspect the whole retina on 10x
2. Find the ventral (biggest) cut and go up
3. Find the optic nerve and set XY coordinates to 0. **Not Z!**
4. Look for a flat area and anotate the XY coordinates
5. Focus on the photorreceptors. 
6. Get out of the retina and focus the **condenser** on the photorreceptors height and set **C** to 0. 
    1. In B, after setting C to zero, focus C to the coordinate you previously registered. 
7. You are ready to record now. 

## Electrode in
8. Put the electrode in, and  lock in positive pressure (~1.3-1.4)
9. Set pippete offset (you should do this everytime a new pipette enters the solution). 

    <img src="..\images\multiclamp.png">
10. Press home in. Move forward in X, then in Y and find the electrode. 

## Tearing the inner limiting membrane
10. Once you have identified a flat area susceptible to recording, you need peel off glial cells end feet (*inner limiting membrane*) with the pipette **without** hurting the ganglion cells. 

- <img src="..\images\membrane_tearing.png" alt="Image Alt Text" width="260" height="500">

- An explanatory video can be found [here](https://www.youtube.com/watch?v=Epfpnh1jxaU) 

## Cell Attached Recording 

11. Once you have identified a cell, play play lightstep in symphony. 
12. Approach the electrode to the cell while constantly giving short pulses of possitve pressure. 
13. Once in the cell, 

## Whole cell patch clamp (work in progress)
 


14. In symphony, run the **Seal and leak** protocol. It should start running the *seal* step. 
The osciloscope should looke like this (but with a single current step, will change the image later.)
- <img src="..\images\scope.png" width="260" height="200"> 
15. Approach to your cell and make the seal, change to leak. 
16. Break the membrane. 

### In multiclamp run the following (color coded with fruitmojis)

17. Change from VC to I=0 and then to IC (&#127815;) 
18. Press auto in Cp fast. (&#x1F34F;)
19. Check your access resistance (	&#129389;).
    - Should be low (30-40 mOhms). A high resistance icreases the series resistance compensation error and decrease thes time resolution of current changes . 
- <img src="..\images\Multiclamp2.png"> 



