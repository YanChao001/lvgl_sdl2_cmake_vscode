file(GLOB lv_drivers_SOURCES *.c display/*.c gtkdrv/*.c indev/*.c)
add_library(lv_drivers ${lv_drivers_SOURCES})
target_include_directories(lv_drivers PUBLIC . display indev)