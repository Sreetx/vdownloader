pkgdatadir = join_paths(get_option('prefix'), get_option('datadir'), meson.project_name())
moduledir = join_paths(pkgdatadir, 'vdownloader')

python = import('python')

conf = configuration_data()
conf.set('PYTHON', python.find_installation('python3').full_path())
conf.set('pkgdatadir', pkgdatadir)
configure_file(
            input: 'vdownloader.in',
           output: 'vdownloader',
    configuration: conf,
          install: true,
      install_dir: get_option('bindir')
)

vdownloader_sources = [
    '__init__.py',
    'main.py'
]

install_data(vdownloader_sources, install_dir: moduledir)
