# PNG `iCCP` tests

These tests check that
PNG files containing an ICC profile
in the `iCCP` chunk
are displayed by applying the ICC profile to the image RGB data
(as [required by the CSS Color 4 specification](https://drafts.csswg.org/css-color-4/#tagged-images))
and not by just throwing the image data at the screen.

Images are in the support directory, as required by WPT.

## Initial, sanity-check tests

Ensure that [untagged images (assumed sRGB)](https://drafts.csswg.org/css-color-4/#tagged-images)
are displayed the same as
[tagged images with an sRGB ICC profile](https://drafts.csswg.org/css-color-4/#tagged-images)
or, equivalently,
as images with an [sRGB chunk](https://w3c.github.io/PNG-spec/#11sRGB).

If either test fails, don't bother with the remaining tests.

 - [`sRGB` chunk, relative colorimetric intent](./tests/sRGB-relcolor.html)
 - [untagged image, must be treated as sRGB](./tests/sRGB-untagged.html)

## Embedded ICC v2 profiles

- [sRGB with red and green colorants swapped](./tests/iCCP-v2-rgswap.html)
- [CIE RGB](./tests/iCCP-v2-CIE-Lstar.html)
- [ProPhoto RGB, gamma 1.8](./tests/iCCP-v2-ProPhoto.html)

## Embedded ICC v4 profiles

- [CIE RGB](./tests/iCCP-v4-CIE-Lstar.html)
- [ProPhoto RGB, gamma 1.8](./tests/iCCP-v4-ProPhoto.html)
- [Display P3](./tests/iCCP-v4-DisplayP3.html)

## Embedded iccMAX profiles

*none yet*
