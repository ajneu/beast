#
# Copyright (c) 2016-2017 Vinnie Falco (vinnie dot falco at gmail dot com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#
# Official repository: https://github.com/boostorg/beast
#

GroupSources(test/extras/include/boost/beast extras)
GroupSources(subtree/unit_test/include/boost/beast extras)
GroupSources(include/boost/beast beast)
GroupSources(test/bench/utf8_checker "/")

add_executable (bench-utf8-checker
    ${BOOST_BEAST_FILES}
    ${EXTRAS_FILES}
    ${TEST_MAIN}
    Jamfile
    bench_utf8_checker.cpp
)

target_link_libraries(bench-utf8-checker
    Boost::system
)

set_property(TARGET bench-utf8-checker PROPERTY FOLDER "tests-bench")
