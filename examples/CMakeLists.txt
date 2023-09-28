
link_libraries(
		gstrtspserver
		gstrtp-1.0
		gstsdp-1.0
		gstapp-1.0
		gstnet-1.0
)

set (SRC_LIST test-launch.c)

add_executable(test-launch ${SRC_LIST})