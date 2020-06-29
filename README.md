
You'll need to create a few folders and files:
* a setup.py file, which is required in order to use pip install
* a folder called 'distributions', which is the name of the Python package
* inside the 'distributions' folder, you'll need the Gaussiandistribution.py file, Generaldistribution.py and an __init__.py file.

Install Setup Tools for Python

    pip install setuptools

Install MapPlotLIb

    pip install MatplotLib

Crate a virtual enviroment to install your package

    python3 -m venv test_env


Activate virtual environment to install package. This is a safe way to test package. You can always delete the test environment with no consequence.

    source test_env/bin/activate


Once everything is set up, install test package and other necessary packages in test environment:

    pip install .

    pip install MatplotLib


Note: You can deactivate your virtual environment by typing:

    deactivate


If everything is set up correctly, pip will install the distributions package into the workspace. You can then start the python interpreter from the terminal typing:
python

Then within the Python interpreter, you can use the distributions package:
from distributions import Gaussian
gaussian_one = Gaussian(25, 2)
gaussian_one.mean
gaussian_one + gaussian_one