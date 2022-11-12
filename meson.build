project('mate-backgrounds',
  version : '1.26.0',
  meson_version: '>= 0.41.0'
  )

i18n = import('i18n')

prefix = get_option('prefix')
datadir = join_paths(prefix, get_option('datadir'))
backgrounddir = join_paths(datadir, 'backgrounds', 'mate')
metadatadir = join_paths(datadir, 'mate-background-properties')

conf = configuration_data()
conf.set('datadir', datadir)

subdir('desktop')
subdir('po')
