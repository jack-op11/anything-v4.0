---
language:
- en
license: creativeml-openrail-m
tags:
- stable-diffusion
- stable-diffusion-diffusers
- text-to-image
- diffusers
inference: true
---

Try out my new mix! - [Pastel Mix](https://huggingface.co/andite/pastel-mix). Thanks.

Yes, it's a shameless plug.

![](https://huggingface.co/andite/Pastel-Mix/resolve/main/example-images/grid-0020.png)
![](https://huggingface.co/andite/pastel-mix/resolve/main/example-images/grid-reimu.png)

-------

<font color="grey">Thanks to [Linaqruf](https://huggingface.co/Linaqruf) for letting me borrow his model card for reference.

# Anything V4

Welcome to Anything V4 - a latent diffusion model for weebs. The newest version of Anything. This model is intended to produce high-quality, highly detailed anime style with just a few prompts. Like other anime-style Stable Diffusion models, it also supports danbooru tags to generate images.

e.g. **_1girl, white hair, golden eyes, beautiful eyes, detail, flower meadow, cumulonimbus clouds, lighting, detailed sky, garden_** 

I think the V4.5 version better though, it's in this repo. feel free 2 try it 

# Gradio

We support a [Gradio](https://github.com/gradio-app/gradio) Web UI to run anything-v4.0:
[![Open In Spaces](https://camo.githubusercontent.com/00380c35e60d6b04be65d3d94a58332be5cc93779f630bcdfc18ab9a3a7d3388/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f25463025394625413425393725323048756767696e67253230466163652d5370616365732d626c7565)](https://huggingface.co/spaces/akhaliq/anything-v4.0)

## 🧨 Diffusers

This model can be used just like any other Stable Diffusion model. For more information,
please have a look at the [Stable Diffusion](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion).

You can also export the model to [ONNX](https://huggingface.co/docs/diffusers/optimization/onnx), [MPS](https://huggingface.co/docs/diffusers/optimization/mps) and/or [FLAX/JAX]().

```python
from diffusers import StableDiffusionPipeline
import torch

model_id = "andite/anything-v4.0"
pipe = StableDiffusionPipeline.from_pretrained(model_id, torch_dtype=torch.float16)
pipe = pipe.to("cuda")

prompt = "hatsune_miku"
image = pipe(prompt).images[0]

image.save("./hatsune_miku.png")
```

## Examples

Below are some examples of images generated using this model:

**Anime Girl:**
![Anime Girl](https://huggingface.co/andite/anything-v4.0/resolve/main/example-1.png)
```
masterpiece, best quality, 1girl, white hair, medium hair, cat ears, closed eyes, looking at viewer, :3, cute, scarf, jacket, outdoors, streets
Steps: 20, Sampler: DPM++ 2M Karras, CFG scale: 7
```
**Anime Boy:**
![Anime Boy](https://huggingface.co/andite/anything-v4.0/resolve/main/example-2.png)
```
1boy, bishounen, casual, indoors, sitting, coffee shop, bokeh
Steps: 20, Sampler: DPM++ 2M Karras, CFG scale: 7
```
**Scenery:**
![Scenery](https://huggingface.co/andite/anything-v4.0/resolve/main/example-4.png)
```
scenery, village, outdoors, sky, clouds
Steps: 50, Sampler: DPM++ 2S a Karras, CFG scale: 7
```

## License

This model is open access and available to all, with a CreativeML OpenRAIL-M license further specifying rights and usage.
The CreativeML OpenRAIL License specifies: 

1. You can't use the model to deliberately produce nor share illegal or harmful outputs or content 
2. The authors claims no rights on the outputs you generate, you are free to use them and are accountable for their use which must not go against the provisions set in the license
3. You may re-distribute the weights and use the model commercially and/or as a service. If you do, please be aware you have to include the same use restrictions as the ones in the license and share a copy of the CreativeML OpenRAIL-M to all your users (please read the license entirely and carefully)
[Please read the full license here](https://huggingface.co/spaces/CompVis/stable-diffusion-license)

## Big Thanks to

- [Linaqruf](https://huggingface.co/Linaqruf). [NoCrypt](https://huggingface.co/NoCrypt), and Fannovel16#9022 for helping me out alot regarding my inquiries and concern about models and other stuff.