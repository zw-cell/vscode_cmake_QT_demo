aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} APP_SOURCE) # 函数用于收集指定目录下的所有源文件，并将它们存储到一个指定的变量中。
add_executable(demo) 
target_link_libraries(demo PRIVATE Qt6::Widgets MainWindow)
target_sources(demo PUBLIC ${APP_SOURCE} ${PROJECT_RESOURCE}) # target_sources 命令用于指定要为特定目标编译的源文件。
set_target_properties(demo PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
)
