set(LIB_NAME DragonBonesCPP)

include_directories(
    ${COCOS2DX_ROOT_PATH}/cocos
    ${COCOS2DX_ROOT_PATH}/cocos/base
    ${COCOS2DX_ROOT_PATH}/cocos/platform
    ${COCOS2DX_ROOT_PATH}/external
    ${COCOS2DX_ROOT_PATH}/external/glfw3/include/win32
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src
)

if(WINDOWS)
    include_directories(${COCOS2DX_ROOT_PATH}/external/win32-specific/gles/include/OGLES)
endif()

file(GLOB_RECURSE SOURCE
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/Animation.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/AnimationState.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/BaseTimelineState.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/TimelineState.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/WorldClock.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Armature.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Bone.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Constraint.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/DeformVertices.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Slot.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/TransformObject.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/core/BaseObject.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/core/DragonBones.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/event/EventObject.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/factory/BaseFactory.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Point.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Transform.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/AnimationConfig.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/AnimationData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/ArmatureData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/BoundingBoxData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/CanvasData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/ConstraintData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/DisplayData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/DragonBonesData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/SkinData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/TextureAtlasData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/UserData.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/BinaryDataParser.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/DataParser.cpp
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/JSONDataParser.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCArmatureDisplay.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCFactory.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCSlot.cpp
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCTextureAtlasData.cpp
)
file(GLOB_RECURSE HEADER
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/DragonBonesHeaders.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/Animation.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/AnimationState.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/BaseTimelineState.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/IAnimatable.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/TimelineState.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/animation/WorldClock.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Armature.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Bone.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Constraint.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/DeformVertices.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/IArmatureProxy.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/Slot.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/armature/TransformObject.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/core/BaseObject.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/core/DragonBones.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/event/EventObject.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/event/IEventDispatcher.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/factory/BaseFactory.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/ColorTransform.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Matrix.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Point.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Rectangle.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/geom/Transform.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/AnimationConfig.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/AnimationData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/ArmatureData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/BoundingBoxData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/CanvasData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/ConstraintData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/DisplayData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/DragonBonesData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/SkinData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/TextureAtlasData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/model/UserData.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/BinaryDataParser.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/DataParser.h
    ${CMAKE_CURRENT_LIST_DIR}/DragonBones/src/dragonBones/parser/JSONDataParser.h
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCArmatureDisplay.h
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCDragonBonesHeaders.h
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCFactory.h
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCSlot.h
    ${CMAKE_CURRENT_LIST_DIR}/Cocos2DX_3.x/src/dragonBones/cocos2dx/CCTextureAtlasData.h
)

add_library(${LIB_NAME} STATIC ${SOURCE} ${HEADER})
add_dependencies(${LIB_NAME} cocos2d)

use_cocos2dx_compile_define(${LIB_NAME})
