file(GLOB lvgl_SOURCES src/lv_core/*.c src/lv_draw/*.c src/lv_font/*.c src/lv_gpu/*.c src/lv_hal/*.c src/lv_misc/*.c src/lv_themes/*.c src/lv_widgets/*.c)
add_library(lvgl ${lvgl_SOURCES})
target_include_directories(lvgl PUBLIC .)