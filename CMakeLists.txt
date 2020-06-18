cmake_minimum_required(VERSION 3.15)
project(LearnCMake)

set(CMAKE_CXX_STANDARD 17)

#添加模块
if (USE_MODULE)
    add_subdirectory(LibraryModule)
    list(APPEND EXTRA_LIBS LibraryModule)
endif ()

add_executable(LearnCMake main.cpp test.cpp)

#将模块与项目链接
target_link_libraries(LearnCMake PUBLIC ${EXTRA_LIBS})

#添加头文件
target_include_directories(LearnCMake PUBLIC
        ${PROJECT_SOURCE_DIR}/include)


