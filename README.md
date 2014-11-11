kibana-dpkg
===========

kibana dpkg packaging for debian.

The official kibana configuration files are supplied and only adjusted to the correct paths.

Create source packages step by step:

```
git clone https://github.com/elasticsearch/kibana.git kibana-3.1.2
cd kibana-3.1.2
git checkout v3.1.2
tar czf ../kibana_3.1.2.orig.tar.gz ../kibana-3.1.2
git clone https://github.com/1and1/kibana-dpkg.git debian
cd ..
dpkg-source -b kibana-3.1.2
```

Now the binary package can be built with dpkg-buildpackage or pbuilder the usual way.
