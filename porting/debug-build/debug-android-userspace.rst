
Debugging the Android userspace
===============================

Debugging the Android userspace

Logcat
------

Logcat is a tool that reads

.. code-block:: guess

   /system/bin/logcat

For radio logs

.. code-block:: guess

   /system/bin/logcat -b radio

dmesg
-----

Even though Android logs does not normally end up in dmesg, early initialization of Android and kernel output ends up here.

.. code-block:: guess

   dmesg

Debug Libhybris crash
---------------------

One of the main problems with the current Hybris based architecture, is the lack of symbols resolution and mapping once a crash happens at the Android layer. To workaround this we need to manuly import non stripped libaries
