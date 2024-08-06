# Programming
Programming is a skill that needs to be acquired no matter what engineering front you are working on. Here are some resources to get you started with it.

## Setting up programming Environment

# how to access storage nodes etc can be in Software and computer resources

## IDE - Integrated Development Environment
Gone are the days when we used text editor for writing code. There are now softwares for writing softwares that are called IDE. It includes the compiler, package manager, debugger etc (don't worry if you are not aware of the terms. they are easier than they sound). The choice of IDE is a personal one and people are very opinionated on which IDE is best. The best IDE is the one that you are comfortable using and fits into your workflow

### IntelliJ
The best IDE available for us is IntelliJ – it integrates github, python, has github copilot like features etc. It has debugging capabilities in-built in it and is much better than VSCode. You can download the latest version by requesting a free full-version licence through https://www.jetbrains.com/community/education/#students or opt for the free community edition at https://www.jetbrains.com/idea/download/?section=windows .

### VSCode
The other best and most popular editor to use is Visual Studio Code. VSCode is widely used by developers for its powerful features and flexibility along with being lightweight. VSCode has excellent debugging capabilities and is better than IntelliJ due to the user generated extensions which can improve work efficiency. VSCode can be downloaded here: https://code.visualstudio.com/
Make sure to sign in with your Github Account to sync settings and use Github Copilot.

Recommended Extensions: Jupyter, Python, Python Debugger, Git Graph, GitHub Copilot, GitHub Copilot chat, Pylance.


# Git

For version control you also need to download git: https://git-scm.com/downloads
Git allows for code version control and is used for lab code to enable collaboration.
To manage your git repositories you can use the git command line, download the github desktop app: https://desktop.github.com/download/, or use VSCode's built in Git extension

# Cuda

CUDA (Compute Unified Device Architecture) is a parallel computing platform and application programming interface (API) model created by NVIDIA. It allows developers to use NVIDIA GPUs for general-purpose processing. We use CUDA to train machine learning models and speed up compute. Most of the workstations will have this preinstalled, but if you are running code on a new machine you need to install the CUDA toolkit at https://developer.nvidia.com/cuda-downloads

# GitHub Copilot

GitHub Copilot is an AI-powered code completion tool developed by GitHub in collaboration with OpenAI. It is one of the most recent and powerful tools we have started using which can greatly improve developement efficiency and troubleshooting. To get Copilot you need to apply for a Github Education account here: https://education.github.com/discount_requests/application. This requries you to have your Illinois email on your Github Account and you will have to upload proof that you are a student such as your Illinois ID. It will also check for proximity to campus so you need to be on the Illinois VPN or on the network.

You can access Copilot through the VsCode extension or in IntelliJ

# Python Environment

To program in python you need to install Python. I would recommend installing a package manager such as Anaconda: https://www.anaconda.com/download/success
Anaconda simplifies pacakge management and deployment with environmental management and good pre-installed packages. It also has a grpahica user interface to manage packages.
You can also directly download python from the microsoft store or source website: https://www.python.org/downloads/

### Python Libraries

A Python library is a collection of pre-written code that you can use to perform common tasks, making it easier and faster to develop software. Libraries contain modules, which are files containing Python code that define functions, classes, and variables. By using libraries, you can leverage existing solutions for various tasks such as data manipulation, numerical computations, machine learning, web development, and more, without having to write the code from scratch. If you need code for a specific task it is likely a Google search or Copilot query will point you to a python library that has the code you need. Here are some common libraries we use extensively:

## General Purpose: NumPy
- **Purpose**: Numerical computing.
- **Features**: Provides support for arrays, matrices, and a large collection of mathematical functions to operate on these data structures.
- **Example**:
  ```python
  import numpy as np
  arr = np.array([1, 2, 3])
  print(arr)
  ```

## General Purpose: pandas
- **Purpose**: Data manipulation and analysis.
- **Features**: Offers data structures like DataFrame and Series for handling structured data, along with functions for data cleaning, merging, reshaping, and aggregation.
- **Example**:
  ```python
  import pandas as pd
  df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
  print(df)
  ```

## Plotting: Matplotlib
- **Purpose**: Data visualization.
- **Features**: Provides a wide range of plotting functions to create static, animated, and interactive visualizations.
- **Example**:
  ```python
  import matplotlib.pyplot as plt
  plt.plot([1, 2, 3], [4, 5, 6])
  plt.show()
  ```

## Plotting: Seaborn
- **Purpose**: Statistical data visualization.
- **Features**: Built on top of Matplotlib, it provides a high-level interface for drawing attractive and informative statistical graphics.
- **Example**:
  ```python
  import seaborn as sns
  sns.set(style="darkgrid")
  tips = sns.load_dataset("tips")
  sns.scatterplot(x="total_bill", y="tip", data=tips)
  ```

## Computer Vision: OpenCV
- **Purpose**: Computer vision.
- **Description**: OpenCV (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. It contains more than 2500 optimized algorithms for various computer vision tasks such as image processing, video capture, and analysis, including object detection, face recognition, and camera calibration.

### Example Usage
```python
import cv2

# Read an image from file
img = cv2.imread('image.jpg')

# Convert the image to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Display the grayscale image
cv2.imshow('Gray Image', gray)

# Wait for a key press and close the image window
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Computer Vision: Open3D
- **Purpose**: 3D data processing.
- **Description**: Open3D is an open-source library designed for processing 3D data. It provides data structures and algorithms for 3D data manipulation, including point cloud processing, mesh processing, and 3D visualization. Open3D is widely used in robotics, computer vision, and graphics.

### Example Usage
```python
import open3d as o3d

# Read a point cloud from a file
pcd = o3d.io.read_point_cloud("point_cloud.ply")

# Visualize the point cloud
o3d.visualization.draw_geometries([pcd])
```

## Machine Learning: Scikit-learn
- **Purpose**: Machine learning.
- **Features**: Offers simple and efficient tools for data mining and data analysis, including classification, regression, clustering, and dimensionality reduction.
- **Example**:
  ```python
  from sklearn.ensemble import RandomForestClassifier
  clf = RandomForestClassifier()
  clf.fit(X_train, y_train)
  predictions = clf.predict(X_test)
  ```

## Machine Learning: PyTorch
- **Purpose**: Deep learning.
- **Features**: An open-source machine learning library developed by Facebook's AI Research lab, known for its flexibility and ease of use.
- **Example**:
  ```python
  import torch
  import torch.nn as nn
  import torch.optim as optim
  class Net(nn.Module):
      def __init__(self):
          super(Net, self).__init__()
          self.fc1 = nn.Linear(784, 128)
          self.fc2 = nn.Linear(128, 10)
      def forward(self, x):
          x = torch.relu(self.fc1(x))
          x = torch.softmax(self.fc2(x), dim=1)
          return x
  model = Net()
  criterion = nn.CrossEntropyLoss()
  optimizer = optim.Adam(model.parameters(), lr=0.001)
  ```

## Machine Learning: SciPy
- **Purpose**: Scientific computing.
- **Features**: Builds on NumPy and provides additional functionality for optimization, integration, interpolation, eigenvalue problems, and other advanced mathematical functions.
- **Example**:
  ```python
  from scipy import optimize
  def f(x):
      return x**2 + 5*np.sin(x)
  result = optimize.minimize(f, x0=0)
  print(result)
  ```

