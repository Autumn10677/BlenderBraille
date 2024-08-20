# BlenderBraille
Although many people are considered blind or low vision (BLV), accurate Braille signage can be costly. This problem often results in poor upkeep of Braille signage as it slowly breaks or wears down. Some have attempted to solve this issue by 3D printing their own Braille signage, but often without consideration for the proper grammatical structure or sizing of Braille. Hence, I created an add-on for Blender, a popular 3D modeling software, that would automate Braille generation in a mindful manner of grammar and sizing. I also made an automated tool for generating tactile models to help in my own STEM outreach!

This is my first attempt at creating a Blender add-on, so please feel free to point out bugs, errors, or suggestions as they come up!

## Installation and Usage Tutorial
A video detailing how to use these packages will be published on [Slightly Professional](https://youtube.com/@slightlyprofessional-bt6bi?si=1RJ9oPkoAoaxnlxy) soon!

## Braille Generator

BlenderBraille's first package, ___Braille Generator___, uses [_pybrl_](https://github.com/ant0nisk/pybrl) to convert user-given text into the corresponding Braille text. ___Braille Generator___ extracts the dot locations produced by this package and produces hemispheres at each corresponding location. An external Python package is required for translation since contracted (Grade 2) Braille uses shorthands to represent common words or phrases. While _pybrl_ is reasonably accurate, it is good to check with a professional translator or someone who can read contracted Braille. All dot size parameters are defaulted to those recommended by [the Braille Authority of North America](https://brailleauthority.org/size-and-spacing-braille-characters#:~:text=3.2.,0.057%20inches%20%5B1.44%20mm%5D.), with the ability to adjust sizing slightly. However, users cannot change sizing parameters outside the allowed ranges provided by the Braille Authority of North America. If one plans on 3D printing their Braille, please ensure that you change the scene settings using the "Set Scene Units to MM" button under the Braille Generator tab.

___NOTE:___ Users must ensure that they install _pybrl_ in a way that Blender can access. Installation is separate from the ___Braille Generator___.

## Tactile Model Generator

In the world of STEM outreach, some programs have created tools called _tactile models_ to aid BLV individuals. Typically, tactile models represent flat planes with raised sections to communicate some visual feature (i.e., height, color, brightness, etc.), although they can take on many other forms. This ___Tactile Model Generator___ is focused on this simple case where an image is used to displace a flat surface. A demonstration of one of these models is shown below to demonstrate how this package works.

<br>
<p align="center" width="100%">
    <img width="70%" src="https://github.com/Autumn10677/BlenderBraille/blob/main/example_model.gif">
</p>
<br>

For the best results, the images fed into the ___Tactile Model Generator___ should be greyscale (where the whitest pixels represent the highest heights). This add-on can process RGBA images by converting them into greyscale by averaging the RGB values. The resulting model may exhibit odd artifacts due to this conversion process.
