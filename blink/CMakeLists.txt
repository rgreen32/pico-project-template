add_executable(blink blink.c)

include(../pico_sdk_import.cmake)
include(../pico_extras_import_optional.cmake)

pico_sdk_init()


# pull in common dependencies
target_link_libraries(blink pico_stdlib hardware_i2c pico_cyw43_arch_none)

# create map/bin/hex file etc.
pico_add_extra_outputs(blink)

# add url via pico_set_program_url
example_auto_set_url(blink)
