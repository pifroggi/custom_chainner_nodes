# Custom ChaiNNer Nodes
[ChaiNNer](https://github.com/chaiNNer-org/chaiNNer) is a node-based image processing GUI aimed at making chaining image processing tasks easy and customizable.

Tested with Alpha v0.22.2

## Nodes
### Image Align with Rife
Aligns an Image with a Reference Image using a modified [Rife](https://github.com/megvii-research/ECCV2022-RIFE). Images should have vague alignment before using this Node. Output Image will have the same dimensions as Reference Image. Resize Reference Image to get desired output scale.

Examples: https://slow.pics/c/rqeq3D97

### Wavelet Color Fix
Correct for upscaling model color shift by first separating the image into wavelets of different frequencies, then matching the average color of the Input Image to that of a Reference Image. In general produces better results than the Average Color Fix at the cost of more computation. The Wavelet Color Fix functions are from [sd-webui-stablesr](https://github.com/pkuliyi2015/sd-webui-stablesr/blob/master/srmodule/colorfix.py).

Example transfering DVD colors to upscaled image: https://imgsli.com/MjM5NzM5/0/2

## Installation
Put all files from the "ChaiNNer Nodes" folder into one of these "processing" folders, depending on your ChaiNNer version:
- normal: AppData\Local\chaiNNer\app-0.22.2\resources\src\packages\chaiNNer_pytorch\pytorch\processing
- portable: chaiNNer\resources\src\packages\chaiNNer_pytorch\pytorch\processing

Then restart ChaiNNer and you can already find the new nodes via the search. Documentation for each setting is directly added into the nodes.
An example chain file is available in the "Examples" folder, which does rough alignment > match colors > improve alignment.

<p align="center">
    <img src="Examples/Image Aligner Example.png" width="720" />
</p>
