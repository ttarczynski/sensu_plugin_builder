# sensu_plugin_builder

RPM building container - current tag: ttarczynski/sensu_plugin_builder:0.6

## Contents
- `sensu-plugins.list` - list of sensu plugins from which RPM packages will be built.
- `build_sensu_plugins.sh` - shell script for building sensu plugins

## Usage

The `build_sensu_plugins.sh` should be used inside a `sensu_plugin_builder` container:

```
# mkdir rpm
# chmod 777 rpm
# docker run -v $(pwd)/rpm/:/home/sensu_plugin_builder/rpm/  ttarczynski/sensu_plugin_builder:0.6 ./build_sensu_plugins.sh /home/sensu_plugin_builder/rpm/ sensu-plugins-entropy-checks
```

After running this command you should find plugin RPMs in `./rpm/` directory.
