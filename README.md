# loudspeaker in Simscape™ and Simulink® 

## Overview
The demonstration provides a detailed simulation of a loudspeaker's internal workings, extending up to the diaphragm, while excluding the enclosure and the air interactions at the front of the loudspeaker. The example showcases the feasibility of replicating the Simscape™ loudspeaker functionality as a behavioral model implemented in Laplace domain in Simulink®.

For those interested in further exploration, a search for "MATLAB loudspeaker" on the internet will lead to a resource titled "Loudspeaker Modeling with Simscape™," which has been available since 2021. Subsequent discussions in the professional community have centered on the computational performance of these models.

The comparative analysis is facilitated by the concurrent modeling of the loudspeaker in both Simulink® and Simscape™, allowing for a direct assessment of execution speeds. The model is structured such that Simulink® constitutes the upper portion, while the lower portion is rendered in Simscape™. The scopes integrated within the model confirm that the outputs of both implementations are consistent.

To quantitatively evaluate the temporal efficiency, one might partition the model and independently measure the execution time of each section. This method provides a clear metric for comparing the performance of the two simulation approaches. Here is a summary of the findings regarding the speed of execution: 
1, There is no significant difference between Simulink® and Simscape™ implementations.
2, Using an analog signal source is faster than using a discrete signal source when the solver is in variable step mode.
3, No significant time difference in running the models in accelerator mode or even the rapid accelerator mode.
4, With a discrete signal source the model can then be executed with a solver that is in a fixed-step mode. Running in fixed-step mode is signifcantly faster than in variable step mode.
5, With the models in fixed-step mode they can be compiled into a standalone executable which runs at least 10x faster.

## Files description
speaker_both.slx -- model showing both the Simulink® and the Simscape™ implementation.
speaker_simscape.slx -- model implemented in Simscape only
speaker_simulink.slx -- model implemented in Simulink only

## Reference
Bo rohde Pedersen, "A study of Loudspeaker Design supported by Digital Signal Processing", PhD thesis, Aalborg University, May 2008.
https://www.mathworks.com/help/sps/powersys/ug/increasing-simulation-speed.html

## License
The license is available in the License.txt file in this GitHub repository.

## Relevant Industries
audio components design, audio equipments design, audio loudspeakers

## Relevant Products
 *  Simulink® 
 *  Simscape™

Copyright 2024 The MathWorks, Inc.