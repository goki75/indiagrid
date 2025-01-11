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

## Usage

```python
from indiagrid import WGS84_to_India, India_to_WGS84

# Convert WGS84 to Indian Grid System
result = WGS84_to_India(lat=28.7041, lon=77.1025)
print(result)
# Output: {'Easting': ..., 'Northing': ..., 'Grid': '...'}

# Convert Indian Grid System to WGS84
reverse_result = India_to_WGS84(Eth=..., Nth=..., grid="I")
print(reverse_result)
# Output: {'latitude': ..., 'longitude': ...}
```

## Parameters

### `WGS84_to_India`

- **lat** (float): Latitude in decimal degrees.
- **lon** (float): Longitude in decimal degrees.
- **esterr** (float): Optional easting error adjustment. Default is 0.
- **ntherr** (float): Optional northing error adjustment. Default is 0.

### `India_to_WGS84`

- **Eth** (float): Easting in the Indian grid system.
- **Nth** (float): Northing in the Indian grid system.
- **grid** (str): Grid region (e.g., 'I', 'IIA', etc.).
- **esterr** (float): Optional easting error adjustment. Default is 0.
- **ntherr** (float): Optional northing error adjustment. Default is 0.

## License

This project is licensed under the MIT License.
```

