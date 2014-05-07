cartography
===========

Cartography related things for other projects.

## Source Data
Natural Earth
Cutural
Admin 0 – Countries
v2.0.0

## topojson args

```shell
topojson \
  --out ne_110m_admin_0_countries_simp_0.1.json \
  --id-property su_a3 \
  --simplify-proportion .1 \
  ne_110m_admin_0_countries.shp
```

-o --out output file
--id-property su_a3 / +iso_n3 (coerce to number)
-p --properties properties to retain, default is none; target=source, e.g.
-properties name=NAME (to lowercase)

--spherical (x/y/z)
-s --simplify precision threshold
--simplify-proportion % of points to retain
use 1 or the other

--cartesian (x/y)
Simplify in projected pixel space
--width --height

line simplification
http://bost.ocks.org/mike/simplify/

-q, --quantization, --no-quantization
If you are generating a small static map in the browser, the default quantization factor is 10,000 (-q 1e4) is probably sufficient. This means that there are a maximum of ten thousand differentiable values along each dimension. If you are generating a large high-resolution map, or if you want to allow the user to zoom in and see greater detail, you should increase the quantization factor by at least one or two orders of magnitude: -q 1e5 or -q 1e6.