file(GLOB lv_examples_SOURCES   src/lv_demo_benchmark/*.c src/lv_demo_printer/*.c src/lv_demo_printer/images/*.c 
                                src/lv_demo_stress/*.c src/lv_demo_widgets/*.c src/lv_ex_get_started/*.c src/lv_ex_style/*.c
                                assets/*.c)
add_library(lv_examples ${lv_examples_SOURCES})
target_include_directories(lv_examples PUBLIC .)