bz_sources = [
  'main.c',
  'bz-application.c',
  'bz-window.c',
  'bz-search-widget.c',
  'bz-content-section.c',
  'bz-content-provider.c',
  'bz-yaml-parser.c',
  'bz-section-view.c',
  'bz-browse-widget.c',
  'bz-update-dialog.c',
  'bz-background.c',
  'bz-entry.c',
  'bz-entry-group.c',
  'bz-transaction.c',
  'bz-transaction-view.c',
  'bz-transaction-manager.c',
  'bz-backend.c',
  'bz-flatpak-instance.c',
  'bz-flatpak-entry.c',
  'bz-paintable-model.c',
  'bz-share-dialog.c',
  'bz-preferences-dialog.c',
  'bz-progress-bar.c',
  'bz-review.c',
  'bz-error.c',
]

bz_deps = [
  cc.find_library('m', required: false),
  dependency('gtk4'),
  dependency('libadwaita-1', version: '>= 1.7'),
  dependency('libdex-1', version: '>= 0.9'),
  dependency('flatpak', version: '>= 1.9'),
  dependency('appstream', version : '>= 1.0'),
  dependency('xmlb', version : '>= 0.3.4'),
  dependency('glycin-1', version : '>= 1.0'),
  dependency('glycin-gtk4-1', version : '>= 1.0'),
  dependency('yaml-0.1', version : '>= 0.2.5'),
]

bz_sources += gnome.compile_resources('bz-resources',
  'bazaar.gresource.xml',
  c_name: 'ga'
)

executable('bazaar', bz_sources,
  dependencies: bz_deps,
       install: true,
)
