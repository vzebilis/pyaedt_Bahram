Optimetrics
===========
This module contains all properties and methods needed to create
optimetrics setups.

.. code:: python

    from pyaedt import Hfss
    app = Hfss(specified_version="2022.2",
                 non_graphical=False, new_desktop_session=True,
                 close_on_exit=True, student_version=False)

    # returns the ParametericsSetups Class
    app.parametrics

    # returns the OptimizationSetups Class
    app.optimizations

    # adds an optimization and returns Setup class with all settings and methods
    sweep3 = hfss.opti_optimization.add_optimization(calculation="dB(S(1,1))", calculation_value="2.5GHz")

    ...

.. currentmodule:: pyaedt.modules.DesignXPloration

.. autosummary::
   :toctree: _autosummary
   :nosignatures:

   ParametricSetups
   OptimizationSetups
   SetupParam
   SetupOpti

