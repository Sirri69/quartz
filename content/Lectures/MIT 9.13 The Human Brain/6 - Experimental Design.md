*This lecture continues the exploration in cognitive neuroscience methods, and introduces new topics too.*

## Transcranial Magnetic Stimulation
Transcranial Magnetic Stimulation (TMS) is a non-invasive procedure that uses magnetic fields to stimulate nerve cells in the brain. It's like a 'remote control' for the brain, but instead of using electricity, it uses magnetic fields.

The biggest advantage of TMS is that it is non-invasive **and** can still test for causal role of specific parts in brain.

Here's how it works:

1. A coil is placed on the scalp. This coil generates a magnetic field when current is passed thru it. Look up [Right Hand Rule](https://en.wikipedia.org/wiki/Fleming%27s_right-hand_rule). 
2. This magnetic field passes through the skull and reaches the brain. 
3. The magnetic field can briefly and focally disrupt neural activity in surface regions of cortex, which can affect mood and other aspects of mental health.

![[Pasted image 20230903021831.png]]

TMS is often used when traditional treatments for conditions like depression or anxiety haven't worked. It's generally considered safe, but like all medical procedures, it can have side effects. An important note is that spatial resolution is low ~ 1-2 cm.

A basic problem with TMS is that it cannot reach the deeper regions of the brain. Hence it cannot study FFA. But here's an idea from David Pitcher: *If you cannot zap the region you FFA love, love the region you can.* So instead of working with FFA directly, we can work with OFA, Occipital Face Area, this region is much closer to the surface and performs similar function as FFA, but it is not super specific.

David Pitcher designed a study where the task was to identify whether the two faces are same or not. The subjects were shown two faces, and were zapped at different times after the second presentation.

![[Pasted image 20230903023319.png]]

ROFA is Right Occipital Frontal Area. And this charts shows how zapping the ROFA and Vertex at different time intervals affect. This shows a very important detail that is you can use TMS to find out when exactly is that part involved in the processing of information or stimuli.

![[Pasted image 20230903023652.png]]


## Invasive Studies
But even with all these methods, we still cannot answer these core questions:
![[Pasted image 20230903025410.png]]

Doris Tsao & Winrich Freiwald did invasive studies on monkeys and here's what they learned.

1. What is actually represented in each region and how is it represented? 
	what is the neural code for faces? record response of each of 100s of neurons to each of 100s of stimuli 
2. What is the actual series of computations that extract these representations, and how do those computations unfold over time? 
	watch representations change over time within and across face patches 
3. Anatomical connections of each face region? 
	tracers and other methods reveal precise anatomical connectivity
4. What is the causal role of each region in face perception?
	electrical stimulation targeted to specific regions
5. How does this system get wired up over development?
	raise monkeys without ever letting them see a face
## Subtraction Logic
Subtraction logic in MRI studies, particularly in neurology, involves the process of comparing two or more images taken at different times to identify changes. This is particularly useful in detecting subtle changes in the brain that may not be visible in a single image. Here are the steps to implement subtraction logic in MRI studies:

1. **Image Acquisition**: The first step is to acquire the images. This involves performing an MRI scan of the patient's brain at two different times. The first image serves as the baseline, and the second image is used for comparison.

2. **Image Registration**: The next step is to align the two images. This is necessary because the patient's position in the scanner may not be exactly the same in both scans. Image registration involves transforming the images so that they are in the same spatial orientation.

3. **Image Normalization**: This step involves adjusting the intensity values of the images to a standard scale. This is necessary because the intensity values can vary due to differences in scanner settings or patient positioning.

4. **Subtraction**: Once the images are registered and normalized, the next step is to subtract one image from the other. This will result in a new image that highlights the differences between the two scans.

5. **Image Analysis**: The final step is to analyze the subtracted image. Any areas of change will appear as bright or dark spots on the image. These changes could indicate a variety of conditions, such as tumor growth or shrinkage, stroke, or other neurological conditions.

6. **Interpretation**: The radiologist or neurologist will then interpret the results, taking into account the patient's medical history, symptoms, and other diagnostic tests. The subtraction image can provide valuable information that helps in making a diagnosis or monitoring the progress of a condition.

It's important to note that subtraction logic is not always necessary or appropriate for every MRI study. It's most useful when looking for small changes that may be difficult to see in a single image. Also, the quality of the subtraction image depends on the quality of the original images and the accuracy of the image registration and normalization processes.
## Minimal Pairs
Minimal pairs refer to two conditions in an experiment that are identical in every way, except for one specific factor that is being tested. This concept is crucial in experimental design to ensure that any differences observed are due to the one variable being tested, and not due to other factors. 

For example, if you're studying how the brain perceives snakes, you might show subjects images of snakes and images of something else. If the images of snakes all have grassy backgrounds and the other images do not, this could be a confounding factor - it might be the grass, not the snakes, that the brain is responding to. 

In an ideal scenario, the only difference between the two sets of images would be the presence or absence of a snake. This would make them a minimal pair, allowing you to conclude that any differences in brain activity are due to the perception of snakes. 

However, achieving perfect minimal pairs is often challenging in real-world experiments, and researchers must be careful to consider and control for potential confounding factors.
## Decisions toward an Actual Experiment
1. What exact conditions will you run in each experiment?
2. What task will the subject do in the scanner?
3. Will you have “baseline” conditions? Of what? Why? 
4. Suppose you get to scan ten subjects for one hour each. Will you assign different conditions to different subjects, or have each subject do all conditions?
5. It is not nice to keep the subject going for an hour without a break, so we usually break scans into “runs” of 3-10 minutes. How many “runs” will you include?
6. Which conditions will happen in each run (e.g., 1 condition/ run, or all conditions in each run, or what)?
7. If multiple conditions per run, will they be clumped or interleaved?
8. What rate of presentation?
9. What order of stimuli/conditions within or across runs?
10. How exactly will you analyze your data?

## Blocked (clumped) vs. Event-related (mixed) Trials

Glossary here:
[[Glossary#^04c2d4|Blocked Trials]] , [[Glossary#^61a227|Spaced Mixed Trial]], [[Glossary#^1ed9c1|Rapid Mixed Trial]]

In the image <span style="color:yellow">yellow</span> and <span style="color:red">red</span> are different stimuli in the trial.

![[Pasted image 20230930023612.png]]

Rapid mixed trial is the most desired state we want, but that messes up the BOLD responses as they just get on top of each other, Spaced Mixed Trial let the BOLD responses reset before the next sample is presented.

In this next image, the subject is presented with red and yellow stimuli (which can be an image of a face and then image of a dot) in a rapid mixed trial fashion. Because it is so rapid, on measuring, we get the <span style="color:orange">orange</span> line, not the red and/or yellow. Here the orange line is the sum of all the BOLD responses, red and yellow are the BOLD responses of the individual stimuli.

![[Pasted image 20240127031933.png]]

We need to go back from observing the orange line, to the difference of the red and the yellow lines. Amazingly, the BOLD responses seem to add up *approximately* linearly. As we have a ton of trials, and we know it adds linearly, we can extract the red and yellow values mathematically.

### Use Functional Regions of Interest (fROIs) Defined in Each Subject Individually with a Localizer Scan

Brains differ from one another and so cannot be perfectly aligned. The exact location of the FFA varies from subject to subject. So, if you want to study it, you have to first find it with a localizer scan in each subject, then you can measure its response to new conditions.

## Factorial Designs
So far we have been talking about very basic experimental designs. Manipulating one factor with two levels, so, is this a face or an object, snake vs non-snake, moving vs stationary, etc. But sometimes we need to study more factors, and with more levels or conditions.

In experimental design, a "factor" refers to an independent variable that researchers manipulate to observe its effect on the dependent variable. It's essentially the thing you change in an experiment to see if it has an impact on the outcome.

"Levels" refer to the different conditions or values that a factor can take on. For example, if your factor is "color", the levels might be "red", "blue", and "green".

![[Pasted image 20240127041653.png]]

The image represents a design where they ran with two levels. In first level, the subject is supposed to pay attention on the face or the object. In another, the subject is supposed to pay attention on the rapidly changing letters overlayed over the image of the face or the object.

This allows us to ask the questions like: 

- Does the response (in a given region) depend on attention?
	- You can compare avg BOLD response in both of the tasks, i.e, when the patient is paying attention to the image and to the letter
	- 
- Does the response (in a given region) depend on stimulus category?
	- So the face area will still respond much higher to the images with the face, irrespective of whether the attention is on the letters or not. This helps you answer, Overall is there a part in brain which likes objects more than faces?
	- You can call this the "main effect" of the stimulus type.
- 