K3D_TEST(platform.configuration PYTHON_SCRIPT ${CMAKE_CURRENT_SOURCE_DIR}/platform_configuration.py LABELS platform)

INCLUDE_DIRECTORIES(${k3d_SOURCE_DIR})
INCLUDE_DIRECTORIES(${k3d_BINARY_DIR}/k3dsdk)
INCLUDE_DIRECTORIES(${Boost_INCLUDE_DIRS})

ADD_EXECUTABLE(test-platform-types platform_types.cpp)
K3D_TEST(platform.types TARGET test-platform-types LABELS platform)

ADD_EXECUTABLE(test-platform-floating-point platform_floating_point.cpp)
K3D_TEST(platform.float TARGET test-platform-floating-point LABELS platform)

ADD_EXECUTABLE(test-platform-normalized platform_normalized.cpp)

ADD_EXECUTABLE(test-platform-statistics platform_statistics.cpp)
