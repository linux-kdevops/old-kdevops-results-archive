# kdevops-results-archive

<img src="images/kdevops-archive.png" width=250 align=center alt="kdevops archive logo">

This is a collection of results for tests run with
[kdevops](https://github.com/linux-kdevops/kdevops)
on different kernels. Each user has their own dedicated
namespace.

Just clone this repository onto the directory where the
kdevops git repository is placed and kdevops will automatically
make use of it. To be clear, you should both the kdevops and
kdevops-results-archive directory in the same directory. Do
not put kdevops-results-archive inside the kdevops directory.

# Seeing tarball contents

To see contents you can use something like:

```
tar -tOJf fstests/mcgrof/xfs/libvirt-qemu/20240505-0001/6.9.0-rc6.xz 2>&1 | grep xfs | grep 033
```

# Seeing fstests results

To see fstests results you can use something like this:

```
tar -xOJf fstests/mcgrof/xfs/libvirt-qemu/20240505-0001/6.9.0-rc6.xz 6.9.0-rc6/xfs_reflink_1024/xfs/033.out.bad
tar -xOJf fstests/mcgrof/xfs/libvirt-qemu/20240505-0001/6.9.0-rc6.xz 6.9.0-rc6/xfs_reflink_1024/xfs/033.dmesg
```
