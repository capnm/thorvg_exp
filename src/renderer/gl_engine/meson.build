source_file = [
   'tvgGlCommon.h',
   'tvgGlGeometry.h',
   'tvgGlGpuBuffer.h',
   'tvgGlList.h',
   'tvgGlProgram.h',
   'tvgGlRenderer.h',
   'tvgGlRenderPass.h',
   'tvgGlRenderTask.h',
   'tvgGlShader.h',
   'tvgGlShaderSrc.h',
   'tvgGlGeometry.cpp',
   'tvgGlGpuBuffer.cpp',
   'tvgGlProgram.cpp',
   'tvgGlRenderer.cpp',
   'tvgGlRenderPass.cpp',
   'tvgGlRenderTask.cpp',
   'tvgGlShader.cpp',
   'tvgGlShaderSrc.cpp',
   'tvgGlTessellator.cpp',
   'tvgGlTessellator.h',
]

gles_dep = meson.get_compiler('cpp').find_library('GLESv3', required: false)

if not gles_dep.found()
  gles_dep = meson.get_compiler('cpp').find_library('GLESv2', required: true)
endif

engine_dep += [declare_dependency(
    dependencies        : gles_dep,
    include_directories : include_directories('.'),
    sources             : source_file,
)]
