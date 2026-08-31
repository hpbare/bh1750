if(ESP_PLATFORM)
    idf_component_register(
        SRCS            "bh1750.c"
        INCLUDE_DIRS    "."
    )
else()
    add_library(bh1750 STATIC bh1750.c)
    target_include_directories(bh1750 PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
endif()
