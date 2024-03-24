# NAME

Alien::SeqAlignment::minimap2 - A Perl wrapper for the minimap2 binary executables

# VERSION

version 0.02

# SYNOPSIS

To execute minimap2, you can use the following code:
  use Alien::SeqAlignment::minimap2;
  use Env qw( @PATH );
  unshift @PATH, Alien::SeqAlignment::hmmer3->bin\_dir;

Then you can call the program as:

    Alien::SeqAlignment::minimap2->minimap2      (list of arguments)

# DESCRIPTION

This distribution provides minimap2 so that it can be used by other
Perl distributions that are on CPAN.  The source code will be downloaded
from the github repository and installed in a private location if it is 
not already installed in your system.

# METHODS

## minimap2

    Alien::SeqAlignment::minimap2->minimap2            (list of arguments)

     

Returns the command name for running the CLI version of the minimap2 aligner.
Minimap2 uses a single executable to build the reference index and align the
query sequences. 

# SEE ALSO

- [minimap2](https://github.com/lh3/minimap2)

    Minimap2 is a versatile sequence alignment program that aligns DNA or mRNA 
    sequences against a large reference database. Typical use cases include: 
    (1) mapping PacBio or Oxford Nanopore genomic reads to the human genome; 
    (2) finding overlaps between long reads with error rate up to ~15%; 
    (3) splice-aware alignment of PacBio Iso-Seq or Nanopore cDNA or Direct RNA 
    reads against a reference genome; (4) aligning Illumina single- or 
    paired-end reads; (5) assembly-to-assembly alignment; (6) full-genome 
    alignment between two closely related species with divergence below ~15%.

    For ~10kb noisy reads sequences, minimap2 is tens of times faster than 
    mainstream long-read mappers such as BLASR, BWA-MEM, NGMLR and GMAP. It is 
    more accurate on simulated long reads and produces biologically meaningful 
    alignment ready for downstream analyses. For >100bp Illumina short reads, 
    minimap2 is three times as fast as BWA-MEM and Bowtie2, and as accurate 
    on simulated data. 

- [Alien](https://metacpan.org/pod/Alien)

    Documentation on the Alien concept itself.

- [Alien::Base](https://metacpan.org/pod/Alien::Base)

    The base class for this Alien. The methods in that class allow you to use
    the static and the dynamic edlib library in your code. 

- [Alien::Build::Manual::AlienUser](https://metacpan.org/dist/Alien-Build/view/lib/Alien/Build/Manual/AlienUser.pod)

    Detailed manual for users of Alien classes.

- [Bio::SeqAlignment](https://metacpan.org/pod/Bio::SeqAlignment)

    A collection of tools and libraries for aligning biological sequences 
    from within Perl. 

# AUTHOR

Christos Argyropoulos <chrisarg@gmail.com>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2024 by Christos Argyropoulos.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
