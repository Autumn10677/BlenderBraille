# BlenderBraille
This collection of Blender add-ons allows users to generate tactile models for BLV individuals.

## Motivation
Although many people are considered blind or low vision (BLV), access to accurate Braille signage is exceptionally costly. Some have attempted to solve this issue by 3D printing their own Braille signage, but often without consideration for the proper grammatical structure or sizing of Braille.

## Braille Generator

BlenderBraille's first package ___Braille Generator___ uses [_pybrl_](https://github.com/ant0nisk/pybrl) to convert user-given text into the corresponding Braille text. ___Braille Generator___ extracts the dot locations produced by this package and produces hemispheres

All dot size parameters are defaulted to those recommended by [the Braille Authority of North America](https://brailleauthority.org/size-and-spacing-braille-characters#:~:text=3.2.,0.057%20inches%20%5B1.44%20mm%5D.), with the ability to slightly adjust sizing.

## Tactile Model Generator

In the world of STEM outreach, there are some programs that have created tools called _tactile models_ to aid BLV individuals. Typically, tactile models represent flat planes with raised sections to communicate some visual feature (i.e., height, color, brightness, etc.), although they can take on many other forms. This ___Tactile Model Generator___ is focused on this simple case where an image is used to displace a flat surface. To demonstrate this package at work, a demonstration of one of these models is shown below.
