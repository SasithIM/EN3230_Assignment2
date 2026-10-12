# EN3230 Assignment 2 — ALOHA and CSMA/CA

Simulink models for a packetized PHY/MAC network. In MATLAB, change to this folder so the library, `networkParams.mat`, and `NetworkChannel.m` are on the path. The models were saved in R2025a and need Simulink, Stateflow, and Communications Toolbox.

## Models

- `PacketizedNetworkSimulinkExample.slx` — three-node network. Data flows 1 → 3 → 2 → 1.
- `PacketizedNetwork4Node.slx` — same PHY and MAC settings, with a fourth node. Data flows 1 → 3 → 2 → 4 → 1. Node 4 uses random seed 42.
- `PacketizedNetworkLib.slx` — PHY/MAC library both models link to.

The top-level switch selects ALOHA or CSMA/CA. On open, each model loads `networkParams.mat` and sets `Ts = 1e-7` s. The saved stop time is `200000*Ts` (20 ms).

`NetworkChannel.m` is the multipath channel block. `Car1.png`, `Car2.png`, and `NetworkChannel.png` are the block icons.

The three-node model and the library come from the MathWorks Communications Toolbox example (Copyright 2017–2025 The MathWorks, Inc.).

`*.slxc` and `slprj/` are generated when a model is simulated and are not in this repository.
