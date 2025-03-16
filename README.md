bari@ubuntu24:~$ export GITHUB_USERNAME=YaQQrQ
bari@ubuntu24:~$ cd ${GITHUB_USERNAME}/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ pushd .
~/YaQQrQ/workspace ~/YaQQrQ/workspace
bari@ubuntu24:~/YaQQrQ/workspace$ source scripts/activate
bari@ubuntu24:~/YaQQrQ/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab02.git projects/lab03
Cloning into 'projects/lab03'...
remote: Enumerating objects: 21, done.
remote: Counting objects: 100% (21/21), done.
remote: Compressing objects: 100% (17/17), done.
remote: Total 21 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (21/21), 7.62 KiB | 976.00 KiB/s, done.
Resolving deltas: 100% (2/2), done.
bari@ubuntu24:~/YaQQrQ/workspace$ cd projects/lab03
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git remote remove origin
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab03.git
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ g++ -std=c++11 -I./include -c sources/print.cpp
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ls print.o
print.o
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ nm print.o | grep print
0000000000000000 T _Z5printRKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSo
000000000000002a T _Z5printRKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt14basic_ofstreamIcS2_E
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ar rvs print.a print.o
ar: creating print.a
a - print.o
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ file print.a
print.a: current ar archive
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ g++ -std=c++11 -I./include -c examples/example1.cpp
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ls example1.o
example1.o
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ g++ example1.o print.a -o example1
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ./example1 && echo
hello
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ g++ -std=c++11 -I./include -c examples/example2.cpp
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ nm example2.o
0000000000000000 V DW.ref.__gxx_personality_v0
                 U __gxx_personality_v0
0000000000000000 T main
                 U __stack_chk_fail
                 U _Unwind_Resume
                 U _Z5printRKNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEERSt14basic_ofstreamIcS2_E
                 U _ZNSt14basic_ofstreamIcSt11char_traitsIcEEC1EPKcSt13_Ios_Openmode
                 U _ZNSt14basic_ofstreamIcSt11char_traitsIcEED1Ev
0000000000000000 W _ZNSt15__new_allocatorIcED1Ev
0000000000000000 W _ZNSt15__new_allocatorIcED2Ev
0000000000000000 n _ZNSt15__new_allocatorIcED5Ev
                 U _ZNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEEC1EPKcRKS3_
                 U _ZNSt7__cxx1112basic_stringIcSt11char_traitsIcESaIcEED1Ev
                 U _ZSt21ios_base_library_initv
0000000000000000 r _ZStL19piecewise_construct
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ g++ example2.o print.a -o example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ./example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat log.txt && echo
hello
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf example1.o example2.o print.o
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf print.a
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf example1 example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf log.txt
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat > CMakeLists.txt <<EOF
> cmake_minimum_required(VERSION 3.4)
> project(print)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat >> CMakeLists.txt <<EOF
> set(CMAKE_CXX_STANDARD 11)
> set(CMAKE_CXX_STANDARD_REQUIRED ON)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat >> CMakeLists.txt <<EOF
> add_library(print STATIC \${CMAKE_CURRENT_SOURCE_DIR}/sources/print.cpp)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat >> CMakeLists.txt <<EOF
> include_directories(\${CMAKE_CURRENT_SOURCE_DIR}/include)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake -H. -B_build
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/YaQQrQ/workspace/projects/lab03/_build
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build
[ 50%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[100%] Linking CXX static library libprint.a
[100%] Built target print
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat >> CMakeLists.txt <<EOF
> add_executable(example1 \${CMAKE_CURRENT_SOURCE_DIR}/examples/example1.cpp)
add_executable(example2 \${CMAKE_CURRENT_SOURCE_DIR}/examples/example2.cpp)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat >> CMakeLists.txt <<EOF
> target_link_libraries(example1 print)
> target_link_libraries(example2 print)
> EOF
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/YaQQrQ/workspace/projects/lab03/_build
[ 33%] Built target print
[ 50%] Building CXX object CMakeFiles/example1.dir/examples/example1.cpp.o
[ 66%] Linking CXX executable example1
[ 66%] Built target example1
[ 83%] Building CXX object CMakeFiles/example2.dir/examples/example2.cpp.o
[100%] Linking CXX executable example2
[100%] Built target example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build --target print
[100%] Built target print
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build --target example1
[ 50%] Built target print
[100%] Built target example1
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build --target example2
[ 50%] Built target print
[100%] Built target example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ ls -la _build/libprint.a
-rw-rw-r-- 1 bari bari 2238 Mar 16 12:39 _build/libprint.a
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ _build/example1 && echo
hello
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ _build/example2
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat log.txt && echo
hello
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf log.txt
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git clone https://github.com/tp-labs/lab03 tmp
Cloning into 'tmp'...
remote: Enumerating objects: 91, done.
remote: Counting objects: 100% (30/30), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 91 (delta 23), reused 21 (delta 21), pack-reused 61 (from 1)
Receiving objects: 100% (91/91), 1.02 MiB | 3.85 MiB/s, done.
Resolving deltas: 100% (41/41), done.
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ mv -f tmp/CMakeLists.txt .
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ rm -rf tmp
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cat CMakeLists.txt
cmake_minimum_required(VERSION 3.4)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

option(BUILD_EXAMPLES "Build examples" OFF)

project(print)

add_library(print STATIC ${CMAKE_CURRENT_SOURCE_DIR}/sources/print.cpp)

target_include_directories(print PUBLIC
  $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
  $<INSTALL_INTERFACE:include>
)

if(BUILD_EXAMPLES)
  file(GLOB EXAMPLE_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/examples/*.cpp")
  foreach(EXAMPLE_SOURCE ${EXAMPLE_SOURCES})
    get_filename_component(EXAMPLE_NAME ${EXAMPLE_SOURCE} NAME_WE)
    add_executable(${EXAMPLE_NAME} ${EXAMPLE_SOURCE})
    target_link_libraries(${EXAMPLE_NAME} print)
    install(TARGETS ${EXAMPLE_NAME}
      RUNTIME DESTINATION bin
    )
  endforeach(EXAMPLE_SOURCE ${EXAMPLE_SOURCES})
endif()

install(TARGETS print
    EXPORT print-config
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/ DESTINATION include)
install(EXPORT print-config DESTINATION cmake)
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/bari/YaQQrQ/workspace/projects/lab03/_build
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ cmake --build _build --target install
[100%] Built target print
Install the project...
-- Install configuration: ""
-- Installing: /home/bari/YaQQrQ/workspace/projects/lab03/_install/lib/libprint.a
-- Installing: /home/bari/YaQQrQ/workspace/projects/lab03/_install/include
-- Installing: /home/bari/YaQQrQ/workspace/projects/lab03/_install/include/print.hpp
-- Installing: /home/bari/YaQQrQ/workspace/projects/lab03/_install/cmake/print-config.cmake
-- Installing: /home/bari/YaQQrQ/workspace/projects/lab03/_install/cmake/print-config-noconfig.cmake
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ tree _install
_install
├── cmake
│   ├── print-config.cmake
│   └── print-config-noconfig.cmake
├── include
│   └── print.hpp
└── lib
    └── libprint.a

4 directories, 4 files
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git add CMakeLists.txt
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git commit -m"added CMakeLists.txt"
[master 2c3c704] added CMakeLists.txt
 1 file changed, 36 insertions(+)
 create mode 100644 CMakeLists.txt
bari@ubuntu24:~/YaQQrQ/workspace/projects/lab03$ git push origin master
Username for 'https://github.com': YaQQrQ
Password for 'https://YaQQrQ@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/YaQQrQ/lab03.git/'
