---
title: Tutorial
author: Syauqi Alias
category: Jekyll
layout: post
---

> ##### TIP
>
> This is where I compile things that I have learned that may benefit others (I think). Most of it probably going to be about embedded system and hardware design. 
{: .block-tip }

# Burn a boatloader into Atmega32A

This is a quick guide on how to flash the Atmega32A using Arduino Uno.

Prerequisite:
- Arduino UNO (the programmer)
- wires/jumpers to link Arduino Uno and Atmega32A
- Atmega32A complete with it minimal circuit design (the target)
- GCC compiler and avrdude install (this is optional, for keyboard building purpose)

# Gain in dB (decibels)

Gain in dB (decibels) is a logarithmic way to express ratios, and it's actually pretty intuitive once you get the hang of it.
The basic formula is: Gain (dB) = 10 × log₁₀(Power_out / Power_in)
Here's what makes dB useful:
Key reference points:

$$
\text{Gain (dB)} = 10 \times \log_{10} \left( \frac{\text{Power}_{\text{out}}}{\text{Power}_{\text{in}}} \right)
$$

- 0 dB = no change (output equals input)
- +3 dB ≈ double the power
- +10 dB = 10× the power
- -3 dB ≈ half the power
- -10 dB = 1/10th the power

Why use dB?

The logarithmic scale lets you work with huge ranges of values more easily. Instead of saying "this amplifier multiplies power by 1,000," you say "it has 30 dB gain." You can also add/subtract dB instead of multiplying ratios. If you have two amplifiers with +10 dB and +20 dB gain in series, the total is simply 30 dB.

**Practical tip:** Every +10 dB adds a zero to your power multiplication. So +20 dB = 100×, +30 dB = 1,000×, and so on.

For voltage or amplitude (instead of power), the formula changes slightly to 20 × log₁₀(ratio), which means +6 dB ≈ doubles the voltage.