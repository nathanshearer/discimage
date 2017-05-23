Description:
  DiscImage creates an image of various disc formats.

Usage:
  discimage -i <device> -t <type> -o <basename>

Options:
  -h
    Display this help message and exit.
  -i /dev/sr0
    Input device.
  -o basename
    Output basename.
  -t type
    Specify the type of disc image to create. Supported types are:
      floppy
        An binary image with 512 byte sectors
      cdrom-mode1raw
        A cdrdao bin+cue+toc image.
        2352 Byte CD-ROM Mode 1 Raw Sector Format:
          12 Bytes (Sync Pattern)
          3 Bytes (Address)
          1 Bytes (Mode, 0x01)
          2048 Bytes (Data)
          4 Bytes (Error Detection)
          8 Bytes (Reserved, 0x0000000000000000)
          276 Bytes (Error Correction)
      cdrom-mode1rawsub
        A cdrdao bin+cue+toc image.
        2448 Byte CD-ROM Mode 1 Raw with Subchannels Sector Format:
          12 Bytes (Sync Pattern)
          3 Bytes (Address)
          1 Bytes (Mode, 0x01)
          2048 Bytes (Data)
          4 Bytes (Error Detection)
          8 Bytes (Reserved, 0x0000000000000000)
          276 Bytes (Error Correction)
          96 Bytes (Subcannels)
      dvdrom
        An iso image with 2048 byte sectors

Examples:
  discimage -i /dev/sr0 -t cdrom-mode1rawsub -o disc1
  discimage -i /dev/sr0 -t dvdrom -o S1D1

Version:
  DiscImage 2.0.0.0
  Copyright (C) 2007 Nathan Shearer
  Licensed under GNU General Public License 2.0
