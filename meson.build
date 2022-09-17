project('test_fn', 'cpp',
  version: '0.1',
  default_options: [

    ]
)

cmake = import('cmake')
fn2_opts = cmake.subproject_options()
fn2_opts.add_cmake_defines({
  'FASTNOISE2_NOISETOOL': false,
  'FASTNOISE2_TESTS': false,

  })

fn2_proj = cmake.subproject('FastNoise2', options: fn2_opts)
fn2_dep = fn2_proj.dependency('FastNoise')

executable('test_fn', 
['main.cpp'],
dependencies: [
  fn2_dep
])