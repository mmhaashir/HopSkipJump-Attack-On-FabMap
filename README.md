# HopSkipJump Attack On FabMap

## Introduction <a name="intro"></a>

This project demonstrates how to perform a targetted attack using the HopSkipJump attack technique while injection noise from a seperate image into the target image to misclassify the loop closure in FabMap. We use python and various libraries, including TensorFlow and ART for this purpose.

![dav_image](https://techs0uls.files.wordpress.com/2020/06/qeba.png?w=1024)

## Table of Contents

- [**Introduction**](#intro)
- [**Dependencies**](#dep)
- [**Dataset**](#data)
- [**Installation**](#install)
- [**Usage**](#usage)
- [**Results**](#results)
- [**Contribution**](#contr)
- [**Conclusion**](#conc)

## Dependencies <a name="dep"></a>

To run this code, you will need the following Python libraries:

  - TensorFlow (as tf)
  - Adversarial Robustness Toolbox (ART)
  - Matplotlib (as matplotlib)
  - Requests
  - NumPy
  - PIL (Python Imaging Library)
  - FabMap Linux Binaries

## Dataset <a name="data"></a>

The dataset can be downloaded [here](http://icvl.ee.ic.ac.uk/vbalnt/hpatches/). Download the `hpatches-sequence-release.tar.gz`

## Installation <a name="install"></a>

1. Clone the repository:
   `git clone https://github.com/mmhaashir/HopSkipJump-Attack-On-FabMap.git`
   
2. Install the required dependencies:
   `pip install tensorflow adversarial-robustness-toolbox matplotlib requests numpy pillow`

3. Get the [FabMap Linux Binaries](https://www.robots.ox.ac.uk/~mjc/Software.htm)

## Usage <a name="usage"></a>

To run the HopSkipJump Adversarial Attack:

  1. Open the Jupyter Notebook provided in the project directory.
     
  2. Get the loop closure likelihood of two images using FabMap

  4. Load the pre-trained ImageNet model using TensorFlow.

  5. Select a target image that you want to attack and an image acting as the noise you wish to inject.

  6. Run the attack. The code will generate adversarial images iteratively and display it alongwith the decreased likelihood.

## Results <a name="results"></a>

After running the attack, you will observe that the adversarial image, created by injecting noise into the target image, is misclassified by the pre-trained machine learning model. The generated adversarial image will be displayed. Pass the adversarial image along with the other image again to FabMap and see if the likelihood has been decreased. If so, the attack is successful which means that FabMap is now not able to identify loopclosure as before.

## Contributing <a  name="contr"></a>

Contributions to this project are welcome. If you have suggestions or improvements, please open an issue or submit a pull request.

## Conclusion <a name="conc"></a>

This project showcases the use of TensorFlow and the Adversarial Robustness Toolbox (ART) to perform a HopSkipJump targeted attack while injecting noise from a separate image into the target image. Such attacks emphasize the need for robust machine learning models and highlight potential security risks associated with adversarial examples.

Feel free to experiment with different images, noise patterns, and attack parameters to gain a deeper understanding of targeted attacks and their impact on machine learning and vision systems.
   

   
