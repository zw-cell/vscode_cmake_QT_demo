add_library(MainWindow STATIC MainWindow.cpp)
target_link_libraries(MainWindow PRIVATE Qt6::Widgets)
target_include_directories(MainWindow  INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})