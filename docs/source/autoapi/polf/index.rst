:py:mod:`porf`
==============

.. py:module:: porf


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   open_sta_parser/index.rst
   run_analyser/index.rst


Package Contents
----------------

Classes
~~~~~~~

.. autoapisummary::

   porf.OpenSTAParser
   porf.RunAnalyser




.. py:class:: OpenSTAParser(file_address='25-rcx_sta.rpt')

   Methodology:
   1. Read metadata on the type of file and run this is.
   2. Identify the boundary lines of the table data through regex matching.
   3. Read in table data of the timing performance.
   4. Understand the relevant timing and data parameters.
   5. Extract the relevant timing and data parameters from the

   .. py:method:: read_file_meta_data()


   .. py:method:: configure_frame_id()


   .. py:method:: configure_timing_data_rows()


   .. py:method:: extract_frame_meta_data()


   .. py:method:: extract_timing_data(frame_id=0)


   .. py:method:: calculate_propagation_delay(net_name_in='in', net_name_out='out', timing_data=None)



.. py:class:: RunAnalyser(run_directory=None)

   This class aims to list and perform analysis on all the relevant files in a particular run between all the corners.

   .. py:method:: get_all_rpt_files()


   .. py:method:: extract_metrics_timing()

      For every file in the sta timing file, extract the propagation delay and save the file meta data into a dicitonary.


   .. py:method:: extract_metrics_power()



