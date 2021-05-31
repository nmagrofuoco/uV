# uV
An ARST-invariant multi-stroke recognizer for fast prototyping.

## Description
uV (multi-Vectors) is an algorithm developed to recognize 2D gestures performed on a touch-sensitive surface and characterized by a single touch (e.g., a finger or a digital pen) and one or several strokes (i.e., uni- or multi-strokes). The recognizer combines the $P+'s cloud matching to satisfy Articulation-invariance and the !FTL's local shape distance to satisfy Rotation-, Scale-, and Translation-invariance (ARST-invariance). Articulation-invariance consists of remaining insensitive to variations in the number, the order, and the direction of the strokes that constitute a multi-stroke gesture.

## Get Started
1. Initialize a `uVRecognizer(numShapes)` object where `numShapes` denotes the number of shapes into which gestures are converted (usually, numShapes=8).
2. Add a series of examples for each gesture class via the `addTemplate(points, name)` method where `points` is an array of Point objects and name describes the class of the gesture.
3. Classify a candidate gesture via the `recognize(points)` method where `points` designates an unknown array of Point objects.

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
