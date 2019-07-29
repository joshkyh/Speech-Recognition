# Speech-Recognition
Hosted files for DEV287x-Speech Recognition Systems



# Set up Conda Environment
conda env create --file conda-linux-cntk-py36-environment.yml --name Speech-Recognition

conda activate Speech-Recognition

pip install https://cntk.ai/PythonWheel/GPU/cntk_gpu-2.5.1-cp36-cp36m-linux_x86_64.whl

- python -c "import cntk"

- pip install soundfile argparse numpy

# Set up Openfst (Tested on Ubuntu 16.04)
sudo apt install graphviz

- Goto http://www.openfst.org/twiki/bin/view/FST/FstDownload
- Download  openfst-1.7.3.tar.gz
- tar -xzf openfst-1.7.3.tar.gz 
- cd openfst-1.7.3/ 
- ./configure --enable-far=true
- make -j4
- sudo make install
- echo "export LD_LIBRARY_PATH=${LD_LIBRARY_PATH}:/usr/local/lib" >> ~/.bashrc
- source ~/.bashrc
- fstinfo --help
- pip install openfst
- python -c "import pywrapfst" 

