#
# project: fips_fmt
#
if (NOT FIPS_IMPORT)
  cmake_minimum_required(VERSION 2.8)
  get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
  include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
  fips_setup()
  fips_project(fips-fmt)
endif()

fips_begin_lib(fmt)
    fips_dir(fmt/src GROUP .)
    fips_files(format.cc)
fips_end_lib()
target_include_directories(fmt PUBLIC fmt/include)

if (NOT FIPS_IMPORT)
  fips_finish()
endif()