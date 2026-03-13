add_library(xenia-cpu-backend-a64 STATIC)
xe_platform_sources(xenia-cpu-backend-a64 ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_definitions(xenia-cpu-backend-a64 PRIVATE
  CAPSTONE_HAS_ARM64
)
target_include_directories(xenia-cpu-backend-a64 PRIVATE
  ${PROJECT_SOURCE_DIR}/third_party/capstone/include
)
target_link_libraries(xenia-cpu-backend-a64 PUBLIC capstone fmt oaknut xenia-base xenia-cpu)
xe_target_defaults(xenia-cpu-backend-a64)
