# AML Project: Neural Style Transfer

Term: Fall 2018

- Project title: Neural Style Transfer Implementation and Applications

- Team members

  - Li, Hongyu hl3099@columbia.edu
  - Zheng, Jia jz2891@columbia.edu
  - Hong, Peifeng ph2534@columbia.edu
  - Wu, Di dw2794@columbia.edu

- Project summary: In this project, we did three things. Firstly, we implemented two style transfer algorithms: the original 1 to 1 neural style transfer algorithm (fixed style for a certain image) that was came up with by [Gatys](https://arxiv.org/abs/1508.06576) and fast neural style transfer algorithm (fixed style for arbitrary image) that was proposed by [Johnson](https://arxiv.org/abs/1603.08155). Secondly, we applied the fast algorithm in real-time off a webcam. Lastly, we are built an app demo so that users could upload their own images and design their own styled photos. 

  ![starry_bulter](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/outputs/starry_bulter_alpha_model.png)

- Project environment: We implemented our code by using **TensorFlow eager execution** which is an imperative programming environment that evaluates operations immediately, without building graphs. Eager execution would be default in TensorFlow 2.0, so we use this mode to implement our code. 

  * Implementations: As for the implementation of one-to-one neural style transfer algorithm, we trained our model on Colab. However, as for the implementation of faster neural style transfer algorithm, we trained our model by using GCP due to the computation complexity. 
  * App demo: We created this demo by using Dash which is a Python framework for building analytical web applications.



## For this project we provide:

  - A report that explains our goals and  results. 
  - [Notebook](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/lib/style_transfer_alpha_final.ipynb) that implements 1 to 1 neural style transfer based on [Gatys' paper](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/papers/A%20Neural%20Algorithm%20of%20Artistic%20Style.pdf). 
  - [Notebook](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/lib/style_transfer_beta_final.ipynb) that implements fast neural style transfer based on [Johnson' paper](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/papers/Perceptual%20Losses%20for%20Real-Time%20Style%20Transfer%20and%20Super-Resolution.pdf). 
  - [Notebook](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/blob/master/lib/webcam_final.ipynb) that applies fast style transfer on webcam. 
  - [Files](https://github.com/PeifengHong/Neural-style-transfer-implementation-and-applications/tree/master/dashapp) that implements the app demo of style transfer. 



## How to reproduce our results: 

* Implementation of 1 to 1 neural style transfer: open `style_transfer_alpha_final.ipynb` and run it. This is an end-to-end notebook which means you do not need to revise anything in order to reproduce our results. (*Note: you could run it without GPU*.)
* Implementation of fast neural style transfer:  open `style_transfer_beta_final.ipynb` and run it. This is an end-to-end notebook which means you do not need to revise anything in order to reproduce our results.  (*Note: you should run it with GPU and it would take 1 hour or longer to train.*)
* Webcam application: open `webcam_final.ipynb` and run it. This is an end-to-end notebook which means you do not need to revise anything in order to reproduce our results.  (*Note: you should run it locally because the camera device is required for this application.*)
  * If you want to reproduce the result of *Starry Night*, you do not have to revise the notebook. 
  * If you want to reproduce the result of *Victoire*, you have to replace `beta_model_style_1.h5` with  `beta_model_style_2.h5` everywhere in step 5. 
  * If you want to reproduce the result of *Women at Their Toilette*, you have to replace `beta_model_style_1.h5` with  `beta_model_style_3.h5` everywhere in step 5. 
  * If you want to reproduce the result of *Google Map*, you have to replace `beta_model_style_1.h5` with  `beta_model_style_4.h5` everywhere in step 5. 
* Dash app demo:  Dash app is an interactive web application developed by python. Our dash app project contains six python files and an assets folder with images.They are App.py, Home.py, DIY.py, WebCam.py, About.py and Index.py. To make use of our app, 
> * Clone the dashapp folder
> * Make sure your system has all the required package
> * Open terminal or command line and run following command: python Index.py
> * Home page shows some result of our work, including the starry night style bulter library.
> > * Click the DIY bar of menu, and then upload your image to see the transfered image with starry night style
> > * Click the WebCam bar of menu, and then select one of the three painting, then click start button to see the live video. Press Q to quit the camera. You can try all of the three styles.
> > * About page is the information of our team member.


## References:

[1]  Leon A Gatys，Alexander S Ecker，Matthias Bethge. A neural algorithm of artistic style[J]. arXiv preprint arXiv:1508.06576, 2015. 

[2]  Justin Johnson，Alexandre Alahi，Li Fei-Fei. Perceptual losses for real-time style transfer and super-resolution[C]. Springer，2016:694-711.

[3]  Falong Shen，Shuicheng Yan，Gang Zeng. Meta Networks for Neural Style Transfer[J]. arXiv preprint arXiv:1709.04111, 2017. 

[4]  Francois Chollet. Deep learning with python[M].Manning Publications Co., 2017.

[5]  Waseem Rawat，Zenghui Wang. Deep convolutional neural networks for image classification: A comprehensive review[J]. Neural computation, 2017, 29(9): 2352-2449.

[6]  Andrew Ng. Nuts and bolts of building AI applications using Deep Learning[C]. NIPS，2016.

[7]  Guillaume Berger，Roland Memisevic. Incorporating long-range consistency in CNN-based texture generation[J]. arXiv preprint arXiv:1606.01286, 2016.

[8]  Karen Simonyan，Andrew Zisserman. Very deep convolutional networks for large-scale image recognition[J]. arXiv preprint arXiv:1409.1556, 2014. 

[9]  Ciyou Zhu，Richard H Byrd，Peihuang Lu, etal. Algorithm 778: L-BFGS-B: Fortran subroutines for large-scale bound-constrained optimization[J]. ACM Transactions on Mathematical Software (TOMS), 1997, 23(4): 550-560.

[10] Harish Narayanan Blog: https://harishnarayanan.org/writing/artistic-style-transfer/.

[11] TF tutorial: https://medium.com/tensorflow/neural-style-transfer-creating-art-with-deep-learning-using-tf-keras-and-eager-execution-7d541ac31398. 

[12] Neural Style Transfer Implementation with Tensorflow Graph Mode: https://github.com/Kautenja/a-neural-algorithm-of-artistic-style. 

[13] Fast Style Transfer with Pytorch: https://github.com/jcjohnson/fast-neural-style.
