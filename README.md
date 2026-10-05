# interactor-pixal3d-image-to-textured-mesh

A container image that serves an image-to-3D model which writes a textured mesh with metal and roughness maps.

## What it is for

It turns one image into a mesh in two requests: the first generates the model's latent with
preview renders and their cameras, and the second decodes that latent to a mesh. A latent-space
editor can take the first answer without a decode in between. RFD 1040 owns the packaging, and
`DETAILS.md` carries its contract test.

## Build

```sh
docker build -t interactor-pixal3d-image-to-textured-mesh .
```

The image needs a GPU to run the model. `desktop/` holds the recipe for running the same model
on a local GPU.

## Licence

This repository does not state a licence.
