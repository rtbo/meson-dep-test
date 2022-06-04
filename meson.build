project('meson-dep-test', 'd')

generator = executable('generator', 'generator.d')

generated = custom_target('generated',
    capture: true,
    output: 'generated.d',
    input: 'input.txt',
    command: [
        generator, '@INPUT@'
    ]
)

lib = static_library('lib', generated, 'lib.d',
    include_directories: include_directories('.'),
)
