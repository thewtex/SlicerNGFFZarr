cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(SlicerNGFFZarr)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/SlicerNGFFZarr")
set(EXTENSION_CATEGORY "IO")
set(EXTENSION_CONTRIBUTORS "Matt McCormick (Kitware, Inc)")
set(EXTENSION_DESCRIPTION "Read and write the Open Microscropy Environment (OME) Next Generation File Format (NGFF) Zarr formatted files (OME-Zarr).

OME-Zarr is a cloud-optimized bioimaging file format with international community support.

This extension uses the ngff-zarr Python package to support reading and writing OME-Zarr in 3D Slicer.")
set(EXTENSION_ICONURL "https://www.example.com/Slicer/Extensions/SlicerNGFFZarr.png")
set(EXTENSION_SCREENSHOTURLS "https://www.example.com/Slicer/Extensions/SlicerNGFFZarr/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(OMEZarr)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
