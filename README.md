## Cross-compile Median and Weighted Mean Filter to RISC-V VP platform

This is the project that implements ee6470 homework 4

## Usage
1. Clone the file to ./ee6470 folder (Git Bash)
```properties
git clone https://github.com/wine10001/EE6470_hw4.git riscv-vp
```
2. Open Windows Powershell
```properties
docker run -h ubuntu --rm --cap-add SYS_ADMIN -it -v "C:\\Users\\<Your Username>:/home/user" ee6470/ubuntu-ee6470:latest
```
3. Login
```properties
/usr/local/bin/entrypoint.sh
```
4. Move to build directory
```properties
cd ~/ee6470
```
```properties
source bashrc
```
5. Build the "basic-acc" platform of riscv-vp
```properties
cd riscv-vp/vp/build
```
```properties
cmake ..
```
```properties
make install
```
6. Build Median and Weighted Mean filter software
```properties
cd ~/ee6470
```
```properties
cd riscv-vp/sw/basic-double
```
```properties
make
```
```properties
make sim
```