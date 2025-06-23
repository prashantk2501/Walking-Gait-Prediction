Accurate, real-time identification of gait events is essential
for closed-loop control of wearable robots. This work proposes a
lightweight machine-learning pipeline that detects lift-offs from
two nine-axis Inertial Measurement Units (IMUs) affixed to the
thigh and shank of a human leg. Raw orientation, angular-
velocity, and acceleration streams, sampled at 50 Hz, are seg-
mented into 1 s windows and converted to a 20-feature tensor. Af-
ter normalization and data-augmentation, windows are labeled
offline via a Euler pitch minima heuristic that marks toe-off and
a peak-detection routine that marks toe-offs.
Two recurrent models are compared: a two-layer vanilla re-
current neural network (RNN) and a two-layer gated recurrent
unit (GRU). Trained with Adam and validated on held-out sub-
jects, the GRU attains a mean absolute error around 42 ms across
slow, self-selected, and fast walking speeds—an average 27 %
improvement over the RNN. The results demonstrate that GRU-
based inference can deliver sub-stride precision on resource-
constrained hardware, paving the way for smoother exoskeleton
assistance and granular rehabilitation feedback.
