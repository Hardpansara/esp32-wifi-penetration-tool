idf_component_register(
    SRCS "wsl_bypasser.c"
    INCLUDE_DIRS "interface"
    REQUIRES esp_wifi esp_event
)
target_link_libraries(${COMPONENT_LIB} -Wl,-zmuldefs)