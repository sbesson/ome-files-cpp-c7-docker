.. _ome-files-view:

ome-files view
==============

Synopsis
--------

**ome-files view** [*options*] *file*

Description
-----------

:program:`ome-files view` renders the pixel data of an image file using
OpenGL.

Open an image using :menuselection:`File --> Open`.

.. note::

  Viewing is currently restricted to the first series of an OME-TIFF
  file.  Future releases will extend this to multiple series, and
  additional file formats.

.. note::

   The viewer currently supports viewing of multi-dimensional
   greyscale planes; RGB images are not yet supported.  This will be
   rectified in a future update.

Navigation
----------

The Navigation dock allows navigation between the constituent planes
of an image.  The Plane slider allows the absolute plane number to be
changed, while individual Z, T, C sliders permit the Z slice,
timepoint or channel to be changed, respectively.  These sliders will
only be available for images using these dimensions.  Additional
ModuloZ, ModuloT and ModuloC sliders may be present for images with
Modulo annotations, for example with certain FLIM datasets.

Rendering
---------

The Rendering dock allows the rendering settings to be adjusted.  This
is currently limited to Min and Max sliders to specify the lower and
upper bounds of the display range for linear contrast adjustment.
This range is used to render with a HiLo lookup table.

.. note::

  The rendering settings will be improved in a future update to allow
  alternate lookup tables and per-channel rendering settings.

2D Camera
---------

The view may be zoomed, panned and rotated.  Select the desired
operation using :menuselection:`View --> Zoom`, :menuselection:`View
--> Pan` or :menuselection:`View --> Rotate`, or use the corresponding
toolbar icon.

zoom
  Press and hold the first mouse button anywhere in the image view,
  then drag up or down to zoom out or zoom in, respectively.
pam
  Press and hold the first mouse button anywhere in the image view,
  then drag to move the image.
rotate
  Press and hold the first mouse button anywhere in the image view,
  then drag up or down to rotate the image counterclockwise or
  clockwise, respectively.

Environment
-----------

:envvar:`OME_FILES_OPENGL_DEBUG`
  If set (to any value), create an OpenGL debugging context and
  verbosely log all OpenGL activity

