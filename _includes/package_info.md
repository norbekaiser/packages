## Beschreibung

{{page.description}}


## Installation
```
apt-get install {{page.package_name}}
```

## Pool
```
deb https://packages.norbert-ruehl.de/dist release {{page.pool}}
```


## Verfügbarkeit


| Debian | Jessie | Stretch |
|--------|--------|---------|
| amd64  |    {%if page.DebianJessieAMD64 %} {{page.DebianJessieAMD64}} {% endif %}  | {%if page.DebianStretchAMD64 %} {{page.DebianStretchAMD64}} {% endif %}  |
| armhf  |    {%if page.DebianJessieARMHF %} {{page.DebianJessieARMHF}} {% endif %}  | {%if page.DebianStretchARMHF %} {{page.DebianStretchARMHF}} {% endif %}  |
| arm64  |    {%if page.DebianJessieARM64 %} {{page.DebianJessieARM64}} {% endif %}  | {%if page.DebianStretchARM64 %} {{page.DebianStretchARM64}} {% endif %}  |

| Raspbian | Jessie | Stretch |
|----------|--------|---------|
| armhf  |    {%if page.RaspbianJessieARMHF %} {{page.RaspbianJessieARMHF}} {% endif %}  | {%if page.RaspbianStretchARMHF %} {{page.RaspbianStretchARMHF}} {% endif %}  |

| Ubuntu | Xenial | Bionic |
|--------|--------|--------|
| amd64  |    {%if page.UbuntuXenialAMD64 %} {{page.UbuntuXenialAMD64}} {% endif %}  | {%if page.UbuntuBionicAMD64 %} {{page.UbuntuBionicAMD64}} {% endif %}  |
| armhf  |    {%if page.UbuntuXenialARMHF %} {{page.UbuntuXenialARMHF}} {% endif %}  | {%if page.UbuntuBionicARMHF %} {{page.UbuntuBionicARMHF}} {% endif %}  |
| arm64  |    {%if page.UbuntuXenialARM64 %} {{page.UbuntuXenialARM64}} {% endif %}  | {%if page.UbuntuBionicARM64 %} {{page.UbuntuBionicARM64}} {% endif %}  |
