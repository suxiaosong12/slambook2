project(rgbd)
 
cmake_minimum_required(VERSION 3.10)
 
find_package(Sophus REQUIRED)
 
add_executable(joinMap joinMap.cpp)
 
include_directories(${Sophus_INCLUDE_DIRS})
 
#链接OpenCV库
 
find_package(OpenCV REQUIRED)
 
#添加头文件
 
include_directories( ${OpenCV-INCLUDE_DIRS})
 
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
 
 
find_package(Pangolin REQUIRED)
 
 
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES})
 
 
# Eigen
 
include_directories("/usr/local/include/eigen3")
 
target_link_libraries(joinMap ${Sophus_LIBRARIES} fmt)
 
 
#链接c++14
 
set(CMAKE_CXX_FLAGS "-std=c++14") 