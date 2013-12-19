kibana-dpkg
===========

kibana dpkg packaging for debian.

The official kibana configuration files are supplied and only adjusted to the correct paths.

Create source packages step by step:

```
git clone https://github.com/elasticsearch/kibana.git kibana-3.0.0milestone4
cd kibana-3.0.0milestone4
git checkout v3.0.0milestone4
tar czf ../kibana_3.0.0milestone4.orig.tar.gz ../kibana-3.0.0milestone4
git clone https://github.com/1and1/kibana-dpkg.git debian
cd ..
dpkg-source -b kibana-3.0.0milestone4
```

Now the binary package can be built with dpkg-buildpackage or pbuilder the usual way.
