load('//:buckaroo_macros.bzl', 'buckaroo_deps')
load('//:subdir_glob.bzl', 'subdir_glob')

cxx_library(
  name = 'raw',
  header_namespace = '',
  exported_headers = glob([
    'libraw/**/*.h',
  ]),
  headers = glob([
    'internal/**/*.h',
  ]),
  srcs = glob([
    'src/**/*.cpp',
    'src/**/*.c',
    'internal/**/*.cpp',
  ], exclude = [
    'src/libraw_fuji_compressed.cpp',
    'internal/aahd_demosaic.cpp',
    'internal/wf_filtering.cpp',
    'internal/dht_demosaic.cpp',
  ]),
  deps = buckaroo_deps(),
  visibility = [
    'PUBLIC',
  ],
)
