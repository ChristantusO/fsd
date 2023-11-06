cmake_minimum_required(VERSION 3.5)
project(fsd
        VERSION 3.99.0
        LANGUAGES C CXX)

##########Modified by chris
#add_definitions(-D_CRT_SECURE_NO_WARNINGS
#        -D_CRT_SECURE_NO_DEPRECATE
#        -D_CRT_NONSTDC_NO_WARNINGS
#        -D_CRT_SECURE_NO_WARNINGS_GLOBALS
#        -D_WINSOCK_DEPRECATED_NO_WARNINGS) #Added by chris

###########

add_executable(fsd
        fsd/attributes.h
        fsd/authenticate.c
        fsd/authenticate.h
        fsd/certificate.cpp
        fsd/certificate.h
        fsd/client.cpp
        fsd/client.h
        fsd/clinterface.cpp
        fsd/clinterface.h
        fsd/cluser.cpp
        fsd/cluser.h
        fsd/config.cpp
        fsd/config.h
        fsd/fsd.cpp
        fsd/fsd.h
        fsd/fsdpaths.h
        fsd/global.h
        fsd/interface.cpp
        fsd/interface.h
        fsd/main.cpp
        fsd/manage.cpp
        fsd/manage.h
        fsd/mm.cpp
        fsd/mm.h
        fsd/process.cpp
        fsd/process.h
        fsd/protocol.h
        fsd/server.cpp
        fsd/server.h
        fsd/servinterface.cpp
        fsd/servinterface.h
        fsd/servuser.cpp
        fsd/servuser.h
        fsd/support.cpp
        fsd/support.h
        fsd/sysinterface.cpp
        fsd/sysinterface.h
        fsd/sysuser.cpp
        fsd/sysuser.h
        fsd/user.cpp
        fsd/user.h
        fsd/wprofile.cpp
        fsd/wprofile.h)
##########Modified by chris
if(WIN32)
    target_link_libraries(fsd wsock32 ws2_32)
endif()
###########
set_property(TARGET fsd PROPERTY CXX_STANDARD 14)
set_property(TARGET fsd PROPERTY CXX_STANDARD_REQUIRED ON)
