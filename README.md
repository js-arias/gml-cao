# Cao et al 2017 unrotated paleolandscape model

This model is based on Cao et al. (2017) model
available at [EarthByte page](https://www.earthbyte.org/paleodem-resource-scotese-and-wright-2018/).
The landscape model uses the following convention:

Key | Environment
--- | -----------
  1 | oceanic plateaus
  2 | continental shelf
  3 | lowlands
  4 | highlands
  5 | ice sheets

The model is unrotated to present coordinates
using the [EarthByte plate motion model](https://github.com/js-arias/gm-earthbyte),
so it can be used with any rotation model.
The main reference for the EarthByte model are:
Torsvik et al. 2019;
Young et al. 2019;
Müller et al. 2019;
Cao et al. 2022;
See that papers for additional references of the different rotations.

## Time frame

The landscape model is defined from 400 million years ago
to today,
in time segments of 5 million years.

## Pixelation

The model is available in three resolutions:
e360 (360 pixels in the equatorial ring),
e180,
and e120.

## File descriptions

The model is stored in the file `cao-landscape-unrot-xxx-5.tab`,
in which `xxx` is the pixel resolution,
and 5 is the time resolution (in million years).

A color key,
which is compatible with color-blindness,
and can be used with `plates timepix map` command
is stored in the file `cao-landscape-key.tab`.

## Rotating the model

To rotate the paleolandscape model,
use the command `plates` from the [earth package](https://github.com/js-arias/earth):

```bash
plates timepix --model <your-model> --output <output-landscape-model> cao-landscape-unrot-xxx-5.tab
```

Note that in such cases,
only pixels associated with a current plate will be rotated,
then,
some past features that appears in the original Cao et al. (2017) landscape model
will be lost.

## Citation and data license

This model is the direct process of the Cao et al. (2017) model.
As such,
the original publication should be cited when the model is used.
Relevant papers are given in this file
and provided as bibTeX.

It is not required to cite this repository,
but if you do not include the model in the supplementary material
of your publication,
it might be a good idea to link this repository
and help others to replicate or re-use your analysis.

## Disclaimer

As the models are a product of a pixelation of vectorial models,
it is possible that some pixels will not be defined
particularly in the boundaries of plates.
Depending on the usage given to the models,
this problems will be only annoying
(for example,
a deep ocean pixel in the middle of a continent),
or it can be critical
(if the feature of interest is near this absent pixels).
So be careful when using the models.

## References

Cao, W. et al.
(2017)
Improving global paleogeography since the late Paleozoic using paleobiology.
Biogeosciences, 14, 5425-5439.
DOI: [10.5194/bg-14-5425-2017](https://doi.org/10.5194/bg-14-5425-2017).

Cao, X. et al.
(2022).
A deforming plate tectonic model of the South China Block since the Jurassic.
Gondwana Research, 102, 3-16.
DOI: [10.1016/j.gr.2020.11.010](https://doi.org/10.1016/j.gr.2020.11.010).

Müller, R. D. et al.
(2019).
A global plate model including lithospheric deformation along major rifts and orogens since the Triassic.
Tectonics, 38, 1884-1907.
DOI: [10.1029/2018TC005462](https://doi.org/10.1029/2018TC005462).

Torsvik, T. H. et al.
(2019).
Pacific‐Panthalassic reconstructions: Overview, errata and the way forward.
Geochemistry, Geophysics, Geosystems, 20, 3659-3689.
DOI: [10.1029/2019GC008402](https://doi.org/10.1029/2019GC008402).

Young, A. et al.
(2019).
Global kinematics of tectonic plates and subduction zones since the late Paleozoic Era. Geoscience Frontiers, 10, 989-1013.
DOI: [10.1016/j.gsf.2018.05.011](https://doi.org/10.1016/j.gsf.2018.05.011).
