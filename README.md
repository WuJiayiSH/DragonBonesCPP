# DragonBones C++ Runtime
[中文 README](./README-zh_CN.md)
## [DragonBones common library](./DragonBones/)
## Highly suggest use [DragonBones Pro](http://www.dragonbones.com/) to create aniamtion.

## Integrate with CMakes

    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP)
    target_link_libraries(${APP_NAME} DragonBonesCPP)
    target_include_directories(${APP_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP/DragonBones/src)
    target_include_directories(${APP_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP/Cocos2DX_3.x/src)

## Supported engines
* [Cocos2d-x](http://cocos2d-x.org/) - [How to use DragoBones in Cocos2d-x](./Cocos2DX_3.x/)
* [SFML](https://www.sfml-dev.org/) - REMOVED! Checkout https://github.com/DragonBones/DragonBonesCPP if you use SFML.

## To learn more about
* [DragonBones offical website](http://www.dragonbones.com/)

## Online demos
[![PerformanceTest](https://dragonbones.github.io/demo/demos.jpg)](https://github.com/DragonBones/Demos)

Copyright (c) 2012-2018 The DragonBones team and other contributors.
