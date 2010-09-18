Usage: png8 [options] <path>...

Uses pngquant and/or pngnq to easily convert images to 8-bit png. The file(s)
is overwritten and a backup is created with a .backup.png extension.

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -p, --preview         preview the original and converted png in Preview.app
  -O, --nobackup        overwrite original file, without backup. Preview is
                        not available with this option
  -i, --interactive     show preview of available variants and select which
                        one to generate
  -f, --force           convert even if file is already an 8-bit png
  -d DESTINATION, --destination=DESTINATION
                        specify a destination for the generated file(s)

