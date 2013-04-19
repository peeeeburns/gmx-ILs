gmx-ILs
=======

Importing gaff ionic liquids into amber99sb-ildn gromacs

=======

Note: A major problem exists in using this force field to impliment ILs in gromacs and generating top files using pdb2gmx.
      There is a limitation in pdb2gmx that prevents use of multiple dihedral function types in a single system.
      So even though the IL dihedrals are function type 9, pdb2gmx generates top files with function type 3. Therefore,
      the grompp program can never find the dihedral parameters for the given IL atom types. Basically, unless somebody writes
      a script to do this automatically, somebody will have to manually change the resulting top file from pdb2gmx to make
      all IL dihedrals to be type 9.
