Linux BSPs
==========

This git repository includes Linux BSPs pulled from semi-conductor trees such
as NXP or TI with updates from linux-stable.

| BSP               | Vendor | Vendor branch                           | Branch with linux-stable updates       |
| ----------------- | ------ | --------------------------------------- | -------------------------------------- |
| beaglebone-black  | TI     | beaglebone-black/upstream/linux-4.19.y  | beaglebone-black/updates/linux-4.19.y  |
| fsl-ls1043a-rdb   | NXP    | fsl-ls1043a-rdb/upstream/linux-4.19.y   | fsl-ls1043a/updates/linux-4.19.y       |

beaglebone-black
-----------------

The `beaglebone-black/upstream/linux-4.19.y` branch was created from:

| Key     | Value                                                  |
| ------- | ------------------------------------------------------ |
| remote  | git://git.ti.com/processor-sdk/processor-sdk-linux.git |
| branch  | processor-sdk-linux-4.19.y                             |
| version | 4.19.94                                                |

The updates branch (`beaglebone-black/updates/linux-4.19.y`) was created with:

```
git checkout -b beaglebone-black/updates/linux-4.19.y beaglebone-black/upstream/linux-4.19.y
git cherry-pick v4.19.94..v4.19.165
```

fsl-ls1043a-rdb
---------------

The `fsl-ls1043a-rdb/upstream/linux-4.19.y` branch was created from:

| Key     | Value                                                               |
| ------- | ------------------------------------------------------------------- |
| remote  | https://source.codeaurora.org/external/qoriq/qoriq-components/linux |
| branch  | linux-4.19.y                                                        |
| version | 4.19.139                                                            |

The updates branch (`fsl-ls1043a/updates/linux-4.19.y`) was created with:

```
git checkout -b fsl-ls1043a-rdb/updates/linux-4.19.y fsl-ls1043a/upstream/linux-4.19.y
git cherry-pick v4.19.139..4.19.165
```

The `-cip` branch (`fsl-ls1043a-rdb/updates/linux-4.19.y-cip`) was created from the
above branch and with cherry-picks from `linux-4.19.y-cip-rebase`:

```
git checkout -b fsl-ls1043a-rdb/updates/linux-4.19.y-cip fsl-ls1043a-rdb/updates/linux-4.19.y
git cherry-pick v4.19.165..eb36474ff12bc22b3cecd30e857b67276fe6659e
```

where `eb36474ff12bc22b3cecd30e857b67276fe6659e` is the commit for `4.19.165-cip41` on the
`linux-4.19.y-cip-rebase` branch
