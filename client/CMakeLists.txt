add_executable(example_client)

target_sources(
  example_client
  PRIVATE
  main.cpp
)

target_link_libraries(
  example_client
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

