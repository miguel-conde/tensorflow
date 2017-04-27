# Tensorflow
A primer on tensorflow

## Installing tensorflow on Windows

1. **Install ANACONDA on your system following [ANACONDA FOR WINDOWS INSTALL](https://docs.continuum.io/anaconda/install-windows)**.

Nowadays, this will install Python 3.6.

**Hint**: Useful Conda CHEAT SHEET [here](https://docs.continuum.io/anaconda/install-windows)


2. **Create Conda virtual environment for Tensorflow with Python 3.5** (cause till now Tensorflow doesn't works with 3.6)

To avoid uninstalling your Anaconda distribution for Python 3.6 and install a previous release you can create a conda environment for Python=3.5 as in:

```
conda create -n tensorflow python=3.5
```
To activate it:
```
activate tensorflow
```
(Type this on a Windows command line)

3. **Now we're ready to install Tensorflow**. Following [Installing TensorFlow on Windows](https://www.tensorflow.org/install/install_windows), we must choose between a TensorFlow with CPU support only installation and a TensorFlow with GPU support one. To carry on the easier first one:

```
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-1.0.1-cp35-cp35m-win_amd64.whl
```

To validate your installation:


	1. Start a terminal.
	2. If you installed through Anaconda, activate your Anaconda environment.
	3. Inside that terminal, invoke python:

```
C:> python
```

	4. Enter the following short program inside the python interactive shell:

```
>>> import tensorflow as tf
hello = tf.constant('Hello, TensorFlow!') sess = tf.Session() print(sess.run(hello))
```


	5. If the Python program outputs the following, then the installation is successful and you can begin writing TensorFlow programs. 

```
Hello, TensorFlow!
```

BONUS: Yo can also try:
```
curl -sSL https://github.com/fchollet/keras/raw/master/examples/mnist_mlp.py | python
```
(from [Get Started With Keras For Beginners](http://ermaker.github.io/blog/2015/09/08/get-started-with-keras-for-beginners.html))

4. Finally, **start RStudio and install [Tensorflow package](https://rstudio.github.io/tensorflow/)**:

```
devtools::install_github("rstudio/tensorflow"
```

And verify:

```
library(tensorflow)
sess = tf$Session()
hello <- tf$constant('Hello, TensorFlow!')
sess$run(hello)
```

## Tutorials

* [Beginners](https://rstudio.github.io/tensorflow/tutorial_mnist_beginners.html)
* [Advanced](https://rstudio.github.io/tensorflow/tutorial_mnist_pros.html)







