# Read SPA on python

Usage:
```python
spectra, wavelength, title = read_spa(filepath)
```

This python function is based on [LoadSprecta](https://la.mathworks.com/matlabcentral/fileexchange/57904-loadspectra) from matlab. It allows working with FTIR spectrums.

## Example
For importing a lot of file you can use ``pathlib``:

```python
from LoadSpectrum import read_spa
import pathlib
 
basepath = '.'
paths = [str(x) for x in list(pathlib.Path(basepath).rglob('*.spa'))]
print('Files detected: {}'.format(len(paths)))

for path in paths:
  spectra_tmp, wavelength_tmp, title_tmp = read_spa(path)
```

# License
GNU General Public License v3.0 or later

See [COPYING](COPYING) to see the full text.
