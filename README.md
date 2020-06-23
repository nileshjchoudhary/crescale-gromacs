### Notes on the GROMACS implementation

Several branches and tags can be found:
- Tag [v2019.4-crescale](https://github.com/bussilab/crescale-gromacs/releases/tag/v2019.4-crescale)
  is the version used in the manuscript and is based on GROMACS 2019.4.
- Tag [v2019.6-crescale](https://github.com/bussilab/crescale-gromacs/releases/tag/v2019.6-crescale)
  integrates GROMACS updates up to 2019.6.
- Tag [v2020.2-crescale](https://github.com/bussilab/crescale-gromacs/releases/tag/v2020.2-crescale)
  is based on GROMACS 2020.2.
- Branches [release-2019](http://github.com/bussilab/crescale-gromacs/tree/release-2019),
  [release-2020](http://github.com/bussilab/crescale-gromacs/tree/release-2020),
  and [master](http://github.com/bussilab/crescale-gromacs/tree/master) are in sync with the official GROMACS repository.
- Branch [release-2019-crescale](http://github.com/bussilab/crescale-gromacs/tree/release-2019-crescale)
  is based on branch [release-2019](http://github.com/bussilab/crescale-gromacs/tree/release-2019).
- Branch [release-2020-crescale](http://github.com/bussilab/crescale-gromacs/tree/release-2020-crescale)
  is based on branch [release-2020](http://github.com/bussilab/crescale-gromacs/tree/release-2020).
- Branch [mster-crescale](http://github.com/bussilab/crescale-gromacs/tree/master-crescale)
  is based on branch [master](http://github.com/bussilab/crescale-gromacs/tree/master).

The changes in version 2019 are [relatively small](https://github.com/bussilab/crescale-gromacs/compare/release-2019..release-2019-crescale). The added code is basically a copy of the Berendsen code, with some modification. The changes in version 2020 are [slighly more complicated](https://github.com/bussilab/crescale-gromacs/compare/release-2020..release-2020-crescale) since in this version the coordinate update might be done on the GPU only. In this case, it was necessary to add a function to allow scaling of the velocities to be performed on the GPU. Changes on master branch are [similar](https://github.com/bussilab/crescale-gromacs/compare/master..master-crescale) and just required some adjustment to be compatible with master branch.
