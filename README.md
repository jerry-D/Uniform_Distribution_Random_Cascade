![](https://github.com/jerry-D/Bidirectional-Artificial-Neuron/blob/main/ThoughtChip_logo.png)
# Uniform Distribution Random Cascade
OpenSCAD model and .stl files for Uniform Distribution Random Cascade using true binary trees 

(June 28, 2025) The images below show the prototype Uniform Distribution Random Cascade I've been working on the past couple weeks. Note that the 3D renderings shown below were exported out of OpenSCAD in .stl format with a scale factor on all 3 axes of .02 and then imported by Blender to perform the shading.  The .stl files provided in this repository have no scaling.  To familiarize yourself with this design start with OpenSCAD using the source files in this repository.

Image "A" shows a frontal shot.  Note the BB at the top.  The question of course is, assuming that the Uniform Distribution Random Cascade is level on the X-Y plane, which path will the BB take?  Furthermore, will the next BB that is dropped make the same choice as the preceding BB for all 4 stages?  Lastly, does the operator's intention in any way influence the outcome? 
Image "B" is from a closer angle with the sliding access panel partially opened so you can see the piezo-electric transducers mounted immediately above the row of large bin number lettering.
Image "C" is from above looking down into the BB input funnel.

![](https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/Blend_composite_3_crop.png)

![](https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/Blend_composite_4_angle_2_crop.png)

![](https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/Blend_composite_down_angle_crop.png)

One of the challenges to demonstrating the quantum (vacuum state) Information Unfolder shown in the recently issued patent US 12,324,295 as FIG. 8, in particular, the upper half of it (820), including spiker circuits (840), is getting access to multi-million dollar equipment needed to assemble a working nanostructure from carbon nanotubes.  Below is an annotated cropping from patent US 12,324,295 showing FIG. 8, referred to therein as the vacuum state information unfolder.  Except for the spiker circuits, it is formed entirely of the bifurcated bidirectional transistor shown in FIG. 1 of the same patent.

![](https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/DIV_FIGs_both.png)

Two divisional patent applications were filed in May to cover the inventions of FIG. 1 and FIG. 8.  The granted parent patent pertains to the bidirectional artificial neuron shown in FIG. 2.  Below are links to the claims for each of the divisionals. Beneath those to links is a link to the recently granted patent.

https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/DIV1_claims_2nd_Amend.pdf
https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/DIV2_claims_2nd_Amend.pdf
https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/ThoughtChip_US12324295B.pdf

To at least demonstrate the concept of the Information Unfolder of FIG. 8, just a couple weeks ago I got the idea to use something similar to the Galton board or Random Mechanical Cascade (RMC) used by Princeton's Engineering Anomalies Research Lab some years back.  The main issue I had with using the Galton board or RMC is the fact that its distributions are Bell curve distribution, in that the Information Unfolder of FIG. 8 (820) is Uniform (i.e., flat) distribution.

Then I got the idea that I can build a true binary decision tree, macro-world Information Unfolder that has a Uniform distribution.  To design it, I used the open source OpenSCAD 3D modeling software. Final rendering as shown below was done using Blender, also open source.  The finished product (not counting the stand) measures roughly 21" X 18".  It's 3D printed in white nylon using an online 3D printing service.  The face and sliding bin access panel are made from .092" clear polycarbonate sheet from Home Depot.  It uses .177 caliber BBs that are fed into the funnel at the top.  Once a BB enters the system, it encounters 4 stages of bumpers on the way down.  At each bumper the BB has to decide to go left or right to continue down to one of the 16 bins at the base.
After impacting the final bumper at stage 4, the BB falls into either the left or right channel leading to the corresponding bin. On its way down, the BB impacts a piezo-electric transducer mounted at a 20 degree angle just below the inlet of the bin, which in turn, produces an initial voltage spike of about 5ms in duration, followed by lower amplitude ringing for another 40ms or so.

The spike signal is conditioned with capacitor, resistor, and clamping diodes before entering a voltage follower op-amp, whose output may or may not be amplified before entering the input of the bin microcontroller embedded A/D converter.
When making a run, the bin microcontroller has basically only three functions.  

The first is to analyze the spikes generated by that bin's piezo-electric transducer and increment its bin count when the set of spike parameters are met. 

The second function of the bin microcontroller is to report,  via Common Area Network (CAN)  bus, the current count to the master controller when queried by it in a round-robin fashion.

The third function of the bin microcontroller is to update its respective 3-digit LED display to show the current spike count. 

Once the master microcontroller has polled all 16 bin microcontrollers, it reports to the host computer/work station, via USB or Bluetooth, the spike counts for each of the 16 bins.  It then begins the process all over again in a continuous loop until the START button on the back is pressed to clear the current counts and initiate a new run.

Here is a schematic of a proposed spiker circuit for the Uniform Distribution Random Cascade;

![](https://github.com/jerry-D/Uniform_Distribution_Random_Cascade/blob/main/Spiker_circuit.png)

So, what's the point some might ask?  Answer:  because each run is statistically collected and reported via USB or Bluetooth to a computer/workstation, this probabilistic "information" can be used to not only train AI neural network models, but also used as real-time data for such AI models thus trained.  

Meaning, it is entirely possible for an AI properly trained in this way to detect the very subtlest signatures (which are outside of random chance) for remote influence of the BBs by one or more observers/operators during each run. 

Meaning,  if the observers agree in advance of each run that they are to volition the BBs to tend to the left-most bin or right-most bin, for example, and the properly trained AI detects this in the Uniform distribution of each run, this would in fact substantiate the quantum mechanical "observer effect" in the macro-world, however slight it might be.
