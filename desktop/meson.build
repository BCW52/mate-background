# replace @datadir@ and translate
metadata = 'mate-desktop.xml'
i18n.merge_file(metadata,
  input: configure_file(
    input: metadata + '.in.in',
    output: metadata + '.in',
    configuration : conf
    ),
  output: metadata,
  po_dir: '../po',
  data_dirs: '..',
  install: true,
  install_dir: metadatadir
  )

backgrounds = [
  'Astronaut.jpg',
  'Water-lilly.jpg',
  'forest-moss.jpg',
  'forest-river-misty.jpg',
  'gentoo.png',
  'MATE-Stripes-Dark.png',
  'holy-arch.png',
  'bamboo.jpg',
  'linux-kernel-realistic.jpg',
  'Minimal.png',
  'minimal_squares.png',
  'solarized-dark-sudo.jpg',
  'solarized-dragon-kali.png',

]
install_data(backgrounds, install_dir: join_paths(backgrounddir, 'desktop'))
