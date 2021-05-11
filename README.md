fips-fmt
=========

fipsified fmt (https://github.com/fmtlib/fmt)

fips build system: https://github.com/floooh/fips

## How to integrate:

Add the dependency to your fips.yml file:

```yaml
imports:
    fips-fmt:
        git: https://github.com/deadwanderer/fips-fmt
```

Use fmt as dependency in your targets:

```cmake
fips_begin_*(...)
    ...
    fips_deps(fmt)
fips_end_*(...)
```
