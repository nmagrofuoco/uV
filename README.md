# uV
An ARST-invariant multi-stroke recognizer for fast prototyping.

## Description
uV (multi-Vectors) is an algorithm developed to recognize 2D gestures performed on a touch-sensitive surface and characterized by a single touch (e.g., a finger or a digital pen) and one or several strokes (i.e., uni- or multi-strokes). The recognizer combines the $P+'s cloud matching [1] to satisfy Articulation-invariance and the !FTL's local shape distance [2] to satisfy Rotation-, Scale-, and Translation-invariance (ARST-invariance). Articulation-invariance consists of remaining insensitive to variations in the number, the order, and the direction of the strokes that constitute a multi-stroke gesture.

## Get Started
1. Initialize a `uVRecognizer(numShapes)` object where `numShapes` denotes the number of shapes into which gestures are converted (usually, numShapes=8).
2. Add a series of examples for each gesture class via the `addTemplate(points, name)` method where `points` is an array of Point objects and name describes the class of the gesture.
3. Classify a candidate gesture via the `recognize(points)` method where `points` designates an unknown array of Point objects.

## Useful Link
[1] Radu-Daniel Vatavu. 2017. Improving Gesture Recognition Accuracy on Touch Screens for Users with Low Vision. In Proceedings of the 2017 CHI Conference on Human Factors in Computing Systems (CHI '17). Association for Computing Machinery, New York, NY, USA, 4667–4679. DOI:https://doi.org/10.1145/3025453.3025941

[2] Jean Vanderdonckt, Paolo Roselli, and Jorge Luis Pérez-Medina. 2018. !!FTL, an Articulation-Invariant Stroke Gesture Recognizer with Controllable Position, Scale, and Rotation Invariances. In Proceedings of the 20th ACM International Conference on Multimodal Interaction (ICMI '18). Association for Computing Machinery, New York, NY, USA, 125–134. DOI:https://doi.org/10.1145/3242969.3243032

## License
The academic publication for uV, and what should be used to cite it, is:

In press.

BSD 3-Clause License

Copyright (c) 2021, Nathan Magrofuoco, Jean Vanderdonckt, and Paolo Roselli
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its
   contributors may be used to endorse or promote products derived from
   this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
