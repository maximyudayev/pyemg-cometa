# Python Binding for Cometa WavePlus Mini Wave and Pico sEMG devices 

Python SDK to interface the [Cometa WavePlus](https://www.cometasystems.com/waveplus/) commercial Mini Wave or Pico sEMG sensors via the [OEM C# shared libraries](https://www.cometasystems.com/sdk-and-integrations/) for realtime streaming acquisition.

> [!NOTE]
> Cometa WavePlus is a system of up to 16 wearable sEMG sensors, and a receiver base station connected to a Windows PC, with a practical range of ~20 meters. Lost packets are filled by the base station with repeated most recently received values. Ensure the person stays in range or the base station is moved around for this device.

> [!NOTE]
> While [it says](https://www.cometasystems.com/sdk-and-integrations/) that Cometa has a Python integration, it's a community driven package. You can access a work-in-progress Python binding, [pyemg-cometa](https://github.com/maximyudayev/pyemg-cometa), to the C# OEM DLLs that powers this package and is suitable for out-of-the-box realtime streaming acquisition.

## Installation
The package interfaces identically the Mini Wave and the Pico sensors, whichever are on and connected to the Cometa WavePlus base station.

Install WavePlus drivers (`EmgMDrivers` and `EmgMUsbDrivers`) for Windows after registering on the [Cometa website](https://www.cometasystems.com/my-account/).

> [!NOTE]
> The latest distributed sEMG drivers marked for Windows 8.1 are compatible with Windows 10/11 and have been validated. The distributed USB drivers marked for Windows 10 are also compatible Windows 11.

### From PyPI
```bash
pip install pysio-pyemg-cometa
```

### From source
```bash
git clone https://github.com/maximyudayev/pyemg-cometa.git
pip install -e pyemg-cometa
```

## Usage
Verify in EMG Motion Tools Windows desktop application that sensors are attached, impedance is checked, and the qulity of the signal is good. Close the application.

> [!IMPORTANT]
> Only 1 connection to the base station can be done at a time, either EMG Motion Tools app, or HERMES. Else the device won't connect.

## Citation
When using any parts of this repository outside of its intended use, please cite the parent project [HERMES](https://github.com/maximyudayev/hermes).
