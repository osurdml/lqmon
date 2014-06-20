lqmon
=====
_A wireless link quality monitor_

This package consists of two parts: a network device monitor that tracks the
aforementioned link quality metrics, and a traffic generator. The device
monitor can be used as a standalone node in any system needing link quality
measurements. The traffic generator generates pseudorandom traffic with which
to stress a network connection.

Purpose
-------
If we can correlate the link quality of an established link and the bandwidth
of that link, perhaps we could estimate the bandwidth of any other access point
without establishing a link.

Being able to predict or communicate the future availability of the currently
online (but not necessarily connected) nodes may be useful for cooperative
robotic exploration.

Notes
-----
A few metrics we could consider to determine link quality (thereby bandwidth):

  * SNR: Signal-to-noise ratio, affected by multipath and interference.
  * Signal strength: Measured in mW or dBm.
  * RSSI: Received Signal Strength Indicator. Can be defined loosely as the log
    of the received signal strength to some reference power (e.g., 1 mW)
    ([pdf](http://www.cse.buffalo.edu/srds2009/F2DA/f2da09_RSSI_Parameswaran.pdf)),
    but because each wireless chipset manufacturer provides a different
    accuracy and range for this number to mean different levels of "signal
    strength", it cannot be used alone as a measure of link quality.
  * ToA: Time of Arrival, or travel time of a radio signal between two
    transceivers.

cat'ing /proc/net/wireless provides some useful information.

