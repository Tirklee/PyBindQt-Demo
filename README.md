# PyBindQt-Demo

This project demonstrates how to integrate a Python interpreter into a Qt C++ application using pybind11. The application creates a simple GUI with a text edit widget acting as a Python console and a button to execute Python code.

## Prerequisites

* C++17 or later
* Qt 5 or later
* Python 3.12
* pybind11

## **Compile the Project**

Use  `cmake` to build the project. Here is an example using `cmake`:

```bash
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
```

After building the project, you can run the executable:

```bash
./pybindqt or pybindq.exe
```

## Code Overview

### Main Components

* **Python Interpreter Initialization** :
  * The Python interpreter is initialized using [`py::scoped_interpreter guard{}`].
  * The Python path is set to include the directory containing the Python library.
  
* **Qt Application Setup** :
  * A [`QMainWindow`]("Go to definition") is created with a central [`QWidget`].
  * A [`QVBoxLayout`]("Go to definition") is used to layout the widgets.
  * A [`QTextEdit`]("Go to definition") widget acts as a Python console.
  * A [`QPushButton`]("Go to definition") is used to run Python code.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

* [pybind11]("https://github.com/pybind/pybind11")
* [Qt]("https://www.qt.io/")

## Contact

For any questions or suggestions, please open an issue.
