set(src_dir "${CMAKE_CURRENT_SOURCE_DIR}")

file(GLOB main_src ${src_dir}/*.cpp)
file(GLOB main_hdr ${src_dir}/*.h)

add_executable(main-bin ${main_src} ${main_hdr})
set_target_properties(main-bin
        PROPERTIES OUTPUT_NAME main)

#target_link_libraries(main-bin main threadpool ${AUDIO_LIBRARIES})

install(TARGETS main-bin
        RUNTIME DESTINATION bin)