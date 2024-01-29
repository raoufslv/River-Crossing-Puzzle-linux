cmake_minimum_required(VERSION 3.0.0)
project(projet1 VERSION 0.1.0)

# include(CTest)
# enable_testing()

SET(CMAKE_CXX_STANDARD 17)




cmake_policy(SET CMP0072 NEW)
#find_package(OpenGL REQUIRED)
add_executable(projet1 main.cpp shader/shader.cpp glad.c glad.h stb_image.h model/objload.cpp)
target_link_libraries(projet1 glfw)
target_link_libraries(projet1 assimp)
target_link_libraries(projet1 sfml-system sfml-window sfml-graphics sfml-network sfml-audio)

# target_link_libraries(projet1 alc)

target_link_libraries(projet1 ${OPENAL_LIBRARIES})
#TARGET_LINK_LIBRARIES(projet1 OpenGL::GL)
TARGET_LINK_LIBRARIES(projet1 ${CMAKE_DL_LIBS})
# target_link_libraries(projet1 ${OPENGL_gl_LIBRARY})
# target_link_libraries(projet1 ${OPENGL_glu_LIBRARY})