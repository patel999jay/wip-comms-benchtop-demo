protobuf_generate_cpp(PROTO_SRCS PROTO_HDRS ${CMAKE_CURRENT_BINARY_DIR} config.proto)

add_executable(wip_comms_regex main.cpp ${PROTO_SRCS} ${PROTO_HDRS})
target_link_libraries(wip_comms_regex goby_middleware wip_comms_config wip_comms_messages)

project_install_bin(wip_comms_regex)
