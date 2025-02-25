Material and stackup
====================
This section lists material and stackup modules.
These classes cannot be used directly but can be accessed through an app.
Example:



Material management
~~~~~~~~~~~~~~~~~~~
This section describes all material-related classes and methods.

.. currentmodule:: pyaedt.modules

.. autosummary::
   :toctree: _autosummary
   :nosignatures:

   MaterialLib.Materials
   Material.Material
   Material.SurfaceMaterial
   Material.MatProperties
   Material.SurfMatProperties
   Material.MatProperty


.. code:: python

    from pyaedt import Hfss
    app = Hfss(specified_version="2022.2",
                 non_graphical=False, new_desktop_session=True,
                 close_on_exit=True, student_version=False)

    # This call returns the Materials class
    my_materials = app.materials
    # This call returns the Material class
    copper = my_materials["copper"]
    # This property is from the MatProperty class
    copper.conductivity
    ...



Stackup management
~~~~~~~~~~~~~~~~~~
This section describes all layer-related classes and methods used in HFSS 3D Layout (and indirectly in Circuit).

.. currentmodule:: pyaedt.modules

.. autosummary::
   :toctree: _autosummary
   :nosignatures:


   LayerStackup.Layers
   LayerStackup.Layer