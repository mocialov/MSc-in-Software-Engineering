###
### Standard Makefile for Webots controllers
### 
### Platform: Windows, Mac OS X, Linux
### Language: C, C++ and Java
### 
### Authors: Olivier Michel - www.cyberbotics.com
### Revised: Yvan Bourquin - September 30th, 2009.
###
### Uncomment the variables to customize the Makefile

### -----C Sources-----
###
### if your controller uses several C sources files:
# C_SOURCES = my_controller.c my_clever_algo.c my_gui.c

### -----C++ Sources-----
###
### if your controller uses several C++ sources files:
# CPP_SOURCES = my_controller.cpp my_clever_algo.cpp my_gui.cpp
###     or
# CC_SOURCES = my_controller.cc my_clever_algo.cc my_gui.cc

### -----C/C++ Options-----
###
### if special CFLAGS are necessary, for example to set optimization level or
### to find include files:
# CFLAGS=-O3 -I/my_library_path/include
###
### if your controller needs additional libraries:
# LIBRARIES=-L/path/to/my/library -lmy_library -lmy_other_library
###
### if you want to use the C API in your C++ program add:
# USE_C_API=1

### -----Java Options-----
###
### if your Java controller needs additional libraries, you should define
### the CLASSPATH environment variable as explained in the Webots User Guide
# CLASSPATH=relative/mylib.jar

RESOURCES_PATH = $(WEBOTS_HOME)/resources/projects/robots/darwin-op
CFLAGS = -I"$(RESOURCES_PATH)/include"

INCLUDE = -I"$(RESOURCES_PATH)/libraries/managers/include" -I"$(RESOURCES_PATH)/libraries/darwin/darwin/Framework/include"
LIBRARIES = -L"$(RESOURCES_PATH)/libraries/darwin" -ldarwin -L"$(RESOURCES_PATH)/libraries/managers" -lmanagers


#CFLAGS = -I"/Applications/Webots/resources/projects/robots/darwin-op/libraries/managers/include/"
#CFLAGS = -L"/Applications/Webots/resources/projects/robots/darwin-op/libraries/managers/"
#CFLAGS = -lmanagers

#LIBRARIES = "$(RESOURCES_PATH)/lib/managers.a"
#LINK_DEPENDENCIES = $(RESOURCES_PATH)/lib/managers.a
CXX_SOURCES = darwin-op_team_1.cpp FieldPlayer.cpp GoalKeeper.cpp Player.cpp
JAR_FILE=darwin-op_team.jar

### Do not modify: this includes Webots global Makefile.include
space :=
space +=
WEBOTS_HOME_PATH=$(subst $(space),\ ,$(strip $(subst \,/,$(WEBOTS_HOME))))
include $(WEBOTS_HOME_PATH)/resources/Makefile.include
