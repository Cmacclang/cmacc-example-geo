# cmacc-example-geo

[![NPM](https://nodei.co/npm/cmacc-example-geo.png?compact=true)](https://nodei.co/npm/cmacc-example-geo/)

This library includes sample addresses. This is used in demo  or test documents.

# About addresses:

A reference to an address is a reference to a Geo.cmacc file located in a given Country > State > County > City > Street > Number directory.

The way to display an address is by using the _adr_12.cmacc file (can be found in country/region specific libraries, for example cmacc-lib-us or cmacc-lib-fr)

For example: 55 Broadway St, Cmabridge, MA 02142 is a _geo.cmacc file created in USA > MA > Middlesex > Broadway St > 55 directory.

The file looks like this: 

```
street_Num = "55";

zip = "02142";

street = [../../BroadwaySt.cmacc];
```

Note that the file references BroadwaySt.cmacc, which contains the info for the street:

```
$ name = "Broadway St";

$ city = [../Cambridge.cmacc];
```

Similarly, the street file references the city it belongs to, Cambridge.cmacc, which itself will reference the country it belongs to, and so on.
Cambridge.cmacc is:

```
$ name = "Cambridge";

$ county = [../Middlesex.cmacc];
```

Middlesex.cmacc is:

```
$ name = "Middlesex";

$ state = [../MA.cmacc];
```

MA.cmacc is:

```
$ name = "Massachusetts";

$ statecode = "MA";

$ flower = "Mayflower";

$ constitution = "Constitution of the Commonwealth of Massachusetts";

$ country = [../USA.cmacc];
```

USA.cmacc is:

```
$ name = "United States of America";
```
