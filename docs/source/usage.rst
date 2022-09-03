Usage
=====

.. _installation:

Installation
------------

To use Bepr package, first install it using pip:

.. code-block:: console

   (.venv) $ pip install bepr

Simulating hosts population
---------------------------

To simulate population of hosts based on the proposed bacteriophage effect resistence model
you can use the ``bepr.simulation()`` and  ``bepr.model_plot()``functions:

.. autofunction:: bepr.simulation

The ``int`` parameter should be a list with the number of initial hosts for respectivelly, Hosts without H. defensa, Hosts with H. defensa without APSE and Hosts with H. defensa with APSE. the parameter ``time`` is the number of model iterations, ``P`` is the number of parasitoids in the system, and the additional arguments are the model parameters as you can see by the example above. Moreover, the ``doplot`` argument allow you to to visualise the dynamics  using this function.

.. autoexception:: bepr.InvalidKindError


For example:

>>> import bepr
>>> teste_values = simulation(init = [500, 500, 2000], time = 1000, P=0,mu = 0.05,th = 0.995, tv = .9, tx = .995, alfa = - np.log(0.285), teta = - np.log(0.9175), beta = 1/105, bh=.2, bv=.3, doplot=False)
>>> model_plot(y=teste_values, save=True, S_name=' MedicagosativaWP.png')

.. image:: ./MedicagosativaWP.png
   :align: center
   :width: 800
   :height: 500
   :alt: Timse Series.

