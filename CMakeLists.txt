project(threadpool CXX)


add_definitions(-lpthread)
include_directories(${PROJECT_SOURCE_DIR})

add_library(threadpool STATIC thrdpool.cpp thrdpool.h list.h)
target_link_libraries(threadpool pthread)

add_executable(test test.cpp)
target_link_libraries(test threadpool)
