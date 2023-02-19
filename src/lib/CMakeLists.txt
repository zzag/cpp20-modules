add_library(foo)
target_sources(foo
    PUBLIC
      FILE_SET cxx_modules TYPE CXX_MODULES FILES
      foo.cxx
)
