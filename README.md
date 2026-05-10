# ddslop
DXT1/DXT5/BC7 DDS texture compressor in pure python, higher quality than texconv's GPU driver

# API
```py

def to_buffer(image, pixel_format=None, mipmaps=True, mipmaps_linear=False, pca=0):
    """Compress a PIL Image to DDS and return the raw bytes.

    Args:
        image:        PIL Image (any mode — converted automatically).
        pixel_format: ``"DXT1"`` (BC1), ``"DXT5"`` (BC3), ``"BC7"`` / ``"BC7lite"``
                      / ``"BC7nano"`` / ``"BC7zero"`` (BPTC).
                      Auto-detected from image mode when *None*.
        mipmaps:      Generate a full mipmap chain down to 1×1 (default True).
        mipmaps_linear: Generate mipmaps in linear light (default False).
        pca:          PCA power-iteration steps for endpoint selection (0 = bbox).
    """
# ...

def save_dds(image, dest, pixel_format=None, mipmaps=True, mipmaps_linear=False, pca=0):
    """Save a PIL Image as a DDS file with BCn compression and mipmaps.

    Args:
        image:        PIL Image (any mode — converted automatically).
        dest:         File path (str / Path) or writable binary file object.
        pixel_format: ``"DXT1"`` (BC1), ``"DXT5"`` (BC3), ``"BC7"`` / ``"BC7lite"``
                      / ``"BC7nano"`` / ``"BC7zero"`` (BPTC).
                      Auto-detected from image mode when *None*.
        mipmaps:      Generate a full mipmap chain down to 1×1 (default True).
        mipmaps_linear: Generate mipmaps in linear light (default False).
        pca:          PCA power-iteration steps for endpoint selection (0 = bbox).
    """
# ...
```

# Quality

TODO

# Usage
See todds for example usage.
