#
# server
#
add_executable(uvweb-server)
target_sources(uvweb-server PRIVATE ServerOptions.cpp UvwebServer.cpp)
target_link_libraries(uvweb-server uvweb ${CONAN_LIBS})

#
# client
#
add_executable(uvweb-client)
target_sources(uvweb-client PRIVATE ClientOptions.cpp UvwebClient.cpp)
target_link_libraries(uvweb-client uvweb  ${CONAN_LIBS})

#
# ws client
#
add_executable(uvweb-ws-client)
target_sources(uvweb-ws-client PRIVATE WsClientOptions.cpp UvwebWsClient.cpp)
target_link_libraries(uvweb-ws-client uvweb ${CONAN_LIBS})

#
# pulsar client
#
add_executable(uvweb-pulsar-client)
target_sources(uvweb-pulsar-client PRIVATE PulsarOptions.cpp UvPulsarClient.cpp)
target_link_libraries(uvweb-pulsar-client uvweb ${CONAN_LIBS})
