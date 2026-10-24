# yamsap third-party source

yamsap ships a few open-source programs and libraries whose licenses ask for
their source code to be available wherever yamsap can be downloaded. They are
FFmpeg, Chromaprint's fpcalc, cliairplay, mutagen, Unidecode and, on Linux
x86_64, libquadmath. This repository holds that source.

Every yamsap release has a release here with the same name. Its files are the
exact source of the versions that release ships, plus the scripts that
configure and build them. `SOURCES.md` in each release lists every file, its
license and its sha256.

yamsap runs these programs, and the programs that load these libraries, as
separate processes. Their licenses don't cover yamsap's own code, and that
code isn't in this repository.

## Rebuilding ffmpeg and fpcalc

Each release's `SOURCES.md` has the exact commands. Copy the four tarballs
into an empty directory, unpack `build-scripts.tar.gz`, and run
`DL_CACHE=<that directory> scripts/build-ffmpeg-fpcalc.sh <output directory>`.
The script checks every tarball's sha256 and needs no network.

## Contact

Write to source@yamsap.com with questions, or to get a copy on physical media.

The build scripts in each release are under the MIT license in `LICENSE`.
Everything else keeps its upstream license, which `SOURCES.md` names.
