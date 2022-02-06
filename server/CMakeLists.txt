add_executable(example_server)

target_sources(
  example_server
  PRIVATE
  main.cpp
)

target_link_libraries(
  example_server
  PRIVATE
  nghttp2
  nghttp2_asio
  Threads::Threads
  OpenSSL::Crypto
  OpenSSL::SSL
  Boost::system
  Boost::thread
  Boost::regex
)

