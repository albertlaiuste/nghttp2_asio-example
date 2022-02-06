### nghttp2_asio example

Depends on:<br />
Boost >= 1.74.0<br />
OpenSSL >= 1.1.1<br />
```
git clone --recursive https://github.com/albertlaiuste/nghttp2_asio-example.git
cd nghttp2_asio-example
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release -GNinja
```
After which you should see the following output:
```
Features:
  Applications:   OFF
  HPACK tools:    OFF
  Libnghttp2_asio:ON
  Examples:       OFF
  Python bindings:OFF
  Threading:      ON
  HTTP/3(EXPERIMENTAL): OFF
```
Continue with:
```
ninja
server/example_server 127.0.0.1 8080 1
client/example_client http://127.0.0.1:8080
```

