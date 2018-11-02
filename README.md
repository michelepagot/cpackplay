[![Build Status](https://travis-ci.com/michelepagot/cpackplay.svg?branch=master)](https://travis-ci.com/michelepagot/cpackplay)   [![Build status](https://ci.appveyor.com/api/projects/status/w3vhd747la12vgyy?svg=true)](https://ci.appveyor.com/project/michelepagot/cpackplay)

# cpackplay
Example project to use cpack and explore its capability
 * CPACK and component to create multiple .zip at once
 * Cross platform NSIS


# Prerequisite
```
sudo apt-get cmake install nsis-pluginapi mingw-w64
```


# Play with it

First test is possibility to generate more than one .zip at once. Key point for this is 
```
set(CPACK_ARCHIVE_COMPONENT_INSTALL ON)
```

So doing... produce two archives
```
mkdir BUILD
cd BUILD
cmake ..
make
make package
```

In order to try not per component behavior try with...
```
cpack -D CPACK_ARCHIVE_COMPONENT_INSTALL=OFF .
```

# Bonus

And Pippo is Italian for Goofy
```
               .
                \ | /
                _\|/_
              .' ' ' '.        ___
            _.|.--.--.|.___.--'___`-.
          .'.'||  |  ||`----'"`   ``'`
        .'.'  ||()|()||
.___..-'.'    /       \
`----'"`     /   .-.   \
            (.'.(___).'.)
             `.__.-.__.'
              |_|   |_|
               `.`-'.'
                 `"`
```