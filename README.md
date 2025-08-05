# milks
MultiLingual Keyword Search (MiLKS) is (going to be) a benchmark for spoken keyword detection in several languages.

## icefall setup
1. Create uv environment and install pip requirements
```sh
uv venv --python=3.13
uv pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
uv pip install git+https://github.com/lhotse-speech/lhotse
```
2. Install [k2 using pre-compiled wheels](https://k2-fsa.github.io/k2/installation/from_wheels.html), ex. for Linux CPU
```sh
uv pip install k2==1.24.4.dev20250714+cpu.torch2.7.1 -f https://k2-fsa.github.io/k2/cpu.html
```
3. Install icefall
```sh
git clone https://github.com/k2-fsa/icefall
cd icefall
uv pip install -r requirements.txt
echo "export PYTHONPATH=$(readlink -f .):$PYTHONPATH" >> ~/.profile
```