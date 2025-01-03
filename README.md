<!-- PROJECT LOGO -->
<p align="center">
  <pre>
______________________   _____ __________________   
\__    ___/\_   _____/  /     \\______   \_____  \  
  |    |    |    __)_  /  \ /  \|     ___//   |   \ 
  |    |    |        \/    Y    \    |   /    |    \
  |____|   /_______  /\____|__  /____|   \_______  /
                   \/         \/                 \/                                   
  </pre>

  <p align="center">
    <br />
    <a href="https://tempo-documentation.readthedocs.io/en/latest/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/username/tempo">View Demo</a>
    ·
    <a href="https://github.com/username/tempo/issues">Report Bug</a>
    ·
    <a href="https://github.com/username/tempo/issues">Request Feature</a>
  </p>
</p>

<!-- Badges -->
<p align="center">
  <a href="https://github.com/oonjnertzern/tempo/actions/workflows/test.yml">
    <img src="https://github.com/oonjnertzern/tempo/actions/workflows/test.yml/badge.svg" alt="Build Status">
  </a>
  <a href="https://github.com/username/tempo/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/username/tempo.svg" alt="License">
  </a>
  <a href="https://github.com/username/tempo/releases">
    <img src="https://img.shields.io/github/v/release/username/tempo.svg" alt="Release">
  </a>
  <a href="https://github.com/username/tempo/stargazers">
    <img src="https://img.shields.io/github/stars/username/tempo.svg" alt="Stars">
  </a>
</p>

<!-- Table of Contents -->
## Table of Contents

- [About TEMPO](#about-tempo)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

# Summary

TEMPO (Time-dependent Evolution of Multiple Pulse Operations) offers accessible and efficient simulations of pulse sequences in Python, using the suite of master equation solvers available in the Quantum Toolbox in Python (QuTiP). 
Besides straightforward definition of pulse sequence structures, including any underlying time-dependent Hamiltonians and pulse timing information, TEMPO enables faster simulations of pulse sequence dynamics (compared to naive implementations using QuTiP) while remaining compatible with the existing collection of QuTiP subpackages. Utilizing the master equation solvers that are native to QuTiP, TEMPO provides two key advantages for numerical simulations of pulse sequence dynamics.


**Ease of Use:** By incorporating both the characteristics of a Hamiltonian and its time constraints as necessary properties, pulses are constructed individually then collated to form a 'pulse sequence'. 
Time evolution is performed without the need to manually deactivate each pulse Hamiltonian outside its given time interval.
Using pulse 'recipes' in TEMPO, the creation of pulses with overlapping functional forms is streamlined, with parameters that can be tuned for individual pulses.

**Faster Executions of Time Evolution:** 
For time evolution, TEMPO organizes each pulse sequence as a series of time segments, preserving only the pulses that are active within each segment.
This avoids overheads incurred by repeated inspections of inactive pulse(s), significantly speeding up evaluation of system evolution.



## Installation

Installation can be done quickly and easily with conda. First, ensure you have setup conda, then follow this tutorial.

1. Run the following to ensure all packages can be discovered. 

```
conda config --append channels conda-forge
```

2. Then build an environment with conda. Make sure you are in the root folder of this project.

```
conda create --name YOUR_ENV_NAME python=3.10.15
conda activate YOUR_ENV_NAME
pip install -r requirements.txt
```

