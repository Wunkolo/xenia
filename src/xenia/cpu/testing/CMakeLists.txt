xe_test_suite(xenia-cpu-tests ${CMAKE_CURRENT_SOURCE_DIR}
  LINKS
    capstone fmt imgui
    xenia-base xenia-core xenia-cpu xenia-gpu
    xenia-kernel xenia-ui xenia-patcher
    $<$<OR:$<STREQUAL:${CMAKE_SYSTEM_PROCESSOR},x86_64>,$<STREQUAL:${CMAKE_SYSTEM_PROCESSOR},AMD64>>:xenia-cpu-backend-x64>
    $<$<STREQUAL:${CMAKE_SYSTEM_PROCESSOR},ARM64>:xenia-cpu-backend-a64>
)
