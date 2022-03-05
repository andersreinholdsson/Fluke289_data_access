**Fluke289_data_access**
A series of Python scripts to access measurements from Fluke 28X meters. Fluke IR Remote Interface required. Created from information provided in Fluke Remote IR documentaton cited in eevblog threads. Buy a Remote Interface from Fluke to access meter data, some come with FlukeView--a form-completion application--that is well worth the money for paid work by skilled technicians.

Getting data from an instrument display for logging can be difficult, if not impossible, without a pathway into the device via GPIB, TCPIP, or other comm port. Messing with JTAG or sniffing the signal is far beyond the capabilities of most folks interested in using the data obtained, so "Hats off" to authors of software for reading and fetching data from an operating meter during measurement. Thanks as well to manufacturers who have provided logging capabilities in their instruments and made them accessible to users. That is the modern way . . .

Some meters are far more locked-down for reasons of security and protection of the customer's perception of the integrity of the data collected. Take Fluke, for example (see Dave's video on why Fluke meters are worth the money, etc.) and the 28X series of meters like my 289. The Fluke business model is that data collection is under the control of the firmware and is presented to the user via remote access thru form-completion software. After a technician logs voltage measurements from some industrial gear over several days, there is a printout with Fluke's name on it to support the log with timestamps for every sample and a whole lot more. Yes, the data is also available for export to CSV files and from there to any analysis, but only via the gateway FormView.

Other than the obvious, why is this a problem? Well, the Fluke 289 has the ability to capture data unattended for days at a time under battery power and preserve a detailed log for later retrieval. It can do this because it sleeps between samples using precious little power and does not rely on disks or tape for storage. 

Other logging meters (Uni-T 61E, for example) will output readings to a PC and MooshiMeter logs via Bluetooth, also to another device. Not even in the same league as Fluke 28X series.

What would be better would be the ability to access the Fluke 289 recorded data directly, 'read-only' of course, much in the same way as getting data from a modern Keithley or Keysight bench meter. To that end, I'm contributing to a long-standing 289 eevblog forum thread:https://www.eevblog.com/forum/reviews/going-further-with-the-fluke-289 

This is not an exercise in 'reverse-engineering' or alternative firmware creation, just a little probing with Python into features documented in the Remote Interface Specification using a Fluke IR USB interface.
