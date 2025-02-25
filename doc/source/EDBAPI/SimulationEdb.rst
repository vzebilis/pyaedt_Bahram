EDB setup
=========
These classes are the containers of ``setup`` classes in EDB for both HFSS and Siwave.


.. code:: python

    from pyaedt import Edb
    edb = Edb(myedb, edbversion="2022.2")

    # this call create a setup and returns the object
    setup = edb.create_hfss_setup("my_setup")
    setup.set_solution_single_frequency()
    setup.hfss_solver_settings.enhanced_low_freq_accuracy = True
    setup.hfss_solver_settings.order_basis = "first"

    setup.adaptive_settings.add_adaptive_frequency_data("5GHz", 8, "0.01")
    ...



.. currentmodule:: pyaedt.edb_core.edb_data

.. autosummary::
   :toctree: _autosummary
   :nosignatures:


   hfss_simulation_setup_data.HfssSimulationSetup
   hfss_simulation_setup_data.EdbFrequencySweep
   hfss_simulation_setup_data.DcrSettings
   hfss_simulation_setup_data.CurveApproxSettings
   hfss_simulation_setup_data.AdvancedMeshSettings
   hfss_simulation_setup_data.ViaSettings
   hfss_simulation_setup_data.DefeatureSettings
   hfss_simulation_setup_data.AdaptiveSettings
   hfss_simulation_setup_data.AdaptiveFrequencyData
   hfss_simulation_setup_data.HfssSolverSettings
   hfss_simulation_setup_data.HfssPortSettings
   hfss_simulation_setup_data.MeshOperationLength
   hfss_simulation_setup_data.MeshOperationSkinDepth
   siwave_simulation_setup_data.SiwaveSYZSimulationSetup
   siwave_simulation_setup_data.SiwaveDCSimulationSetup
