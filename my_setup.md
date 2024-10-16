## Set up environment 
1. [Optional but recommended] Create a new Conda environment. 

    ~~~
    conda create --name CircleNet python=3.6
    ~~~
    
    And activate the environment.
    
    ~~~
    conda activate CircleNet
    ~~~

2. Install Pytorch 0.4.1:
    - Error:The following packages are not available from current channels:

  - pytorch=1.8.2
    ~~~
    conda install pytorch=0.4.1 cuda92 torchvision -c pytorch
    ~~~
    - Solution: 
    ~~~
    conda install pytorch==1.7.1 torchvision cudatoolkit=10.2 -c pytorch
    ~~~

    - Check the torch has been installed correctly
    ~~~
    import torch
    print(torch.__version__)
    ~~~
    or check from terminal command
    ~~~
    python -c "import torch; print(torch.__version__)"
    ~~~

    - I skip the part "And disable cudnn batch normalization(Due to [this issue](https://github.com/xingyizhou/pytorch-pose-hg-3d/issues/16))"
    
    - I remove all of version==x.y.z in the requirement file and install it.