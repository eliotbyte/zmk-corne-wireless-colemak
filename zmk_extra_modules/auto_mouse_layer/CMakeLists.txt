zephyr_library()
zephyr_library_sources(src/auto_mouse_layer.c)
# ZMK's own headers (zmk/event_manager.h, zmk/keymap.h, etc.) live in
# zmk/app/include, which ZMK adds as PRIVATE to the 'app' target.
# External modules don't inherit that, so we add it explicitly here.
zephyr_library_include_directories(${APPLICATION_SOURCE_DIR}/include)
