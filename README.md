[![Build Status](https://travis-ci.com/michelepagot/cpackplay.svg?branch=master)](https://travis-ci.com/michelepagot/cpackplay)

# cpackplay
Example project to use cpack and explore its capability
 * CPACK and component to create multiple .zip at once
 * Cross platform NSIS
 
# Prerequisite
sudo apt-get cmake install nsis-pluginapi mingw-w64
 
# Try it
mkdir BUILD
cd BUILD
cmake ..
make
make package
cpack -D CPACK_COMPONENT_INSTALL=OFF .
