# Indian Grid Converter

A Python library for converting WGS84 latitude and longitude coordinates to the Indian Grid System and vice versa.

## Features

- Convert WGS84 latitude and longitude to the Indian Grid System.
- Convert Indian Grid System coordinates back to WGS84 latitude and longitude.
- Accurate calculations based on the Indian grid system parameters.

## Installation

Install via pip:

```bash
pip install indiagrid
```

Install via GitHub:
```
pip install git+https://github.com/goki75/indiagrid.git
```
## Usage

```python
from indiagrid import wgs84_to_igs, igs_to_wgs84

# Convert WGS84 to Indian Grid System
result = wgs84_to_igs(lat=28.7041, lon=77.1025)
print(result)
# Output: {'Easting': 3632281.67, 'Northing': 531791.54, 'Grid': 'I'}

# Convert Indian Grid System to WGS84
reverse_result = igs_to_wgs84(3632281.67, Nth=531791.54, grid="I")
print(reverse_result)
# Output: {'latitude': 28.704099993002522, 'longitude': 77.10249995658076}
```

## Parameters

### `wgs84_to_igs`

- **lat** (float): Latitude in decimal degrees.
- **lon** (float): Longitude in decimal degrees.
- **esterr** (float): Optional easting error adjustment. Default is 0.
- **ntherr** (float): Optional northing error adjustment. Default is 0.

### `igs_to_wgs84`

- **Eth** (float): Easting in the Indian grid system.
- **Nth** (float): Northing in the Indian grid system.
- **grid** (str): Grid region (e.g., 'I', 'IIA', etc.).
- **esterr** (float): Optional easting error adjustment. Default is 0.
- **ntherr** (float): Optional northing error adjustment. Default is 0.

## License

This project is licensed under the GPLv2 License.
```

