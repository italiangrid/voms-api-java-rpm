# voms-api-java-rpm

The RPM packaging code for VOMS Java APIs version >= 3.0

In order to build the rpm for `voms-java-api` run the following command:
```bash
  make tag=3.x
```

The `tag` parameter specifies the tar or branch of the code that you're 
willing to build.

## Other packaging parameters

- `bcmail_package` : the name of the bcmail package dependency. The default
is the SL6 name, i.e. bouncycastle-mail. Set this to `bouncycastle146-mail` 
when building on SL5.
- `mirror_conf_url` : a URL pointing to a maven settings file that will be included
in the source tarball included in the source rpm. This parameter is necessary
to be able to use snaspshot dependencies and succeed in an ETICS mock repackaging step.
If no value is given, the default maven mirror @ CNAF is used. To use the CERN maven
mirror you can use the following value:
```bash
  make tag=3.x mirror_conf_url=https://raw.github.com/italiangrid/build-settings/master/maven/cern-mirror-settings.xml
```
  

