# K8s demo: mount a PersistentVolumeClaim

This project shows how to use a `PersistentVolumeClaim` with a simple app
deployed on a K8s cluster.

This app is actually a wiki instance powered by [MoinMoin](https://moinmo.in/).
Wiki pages are stored in the container directory `/usr/local/share/moin/data`,
which is mounted on a `PersistentVolume` by the K8s app descriptor.

Deploy this app using this command:
```shell
$ kubectl apply -f moinmoin.yml
```

The app is running a public
[Docker image](https://hub.docker.com/r/olavgg/moinmoin-wiki/) built by
[olavgg](https://github.com/olavgg/moinmoin-wiki).

All pods/services/pvc are created in the namespace `moinmoin`.
