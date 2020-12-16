import os
import torch
import subprocess
print(subprocess.check_output("pip install mmcv-full==latest+torch{} -f https://download.openmmlab.com/mmcv/dist/index.html".format(torch.__version__), shell=True))
!git clone -b master https://github.com/qw61116111/ECG.git 
os.chdir('ECG')
!pip install -r ./requirements/build.txt
!pip install -v -e .
