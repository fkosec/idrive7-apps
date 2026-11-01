# Waze on cluster

The CarPlay map (Waze, Apple Maps or Google Maps) on the instrument cluster of an iDrive 7
car, by Robert Nisipeanu, from
[robertnisipeanu/idrive-apps](https://github.com/robertnisipeanu/idrive-apps) at
`a8f22b8594d7bba0c7b6472ba5431cec6e5ae081`. Install **Waze on cluster** from the Store: it
installs the Waze tool and the cluster renderer first.

**Set Instrument cluster > Central display area to Map view**: the Waze map replaces the stock map while
CarPlay streams it, and the stock map is back when the stream ends or freezes.

| Folder | |
|---|---|
| `robertn_waze_cluster/` | the iDrive app 0.4.1 (Enable map, Disable map, status, the tools' log), a source package the head unit builds |
| `cluster-render/` | the cluster renderer 0.3.2, as published there (`cluster-render@0.3.2.tgz`, sha256 `4fc41e55…`) |
| `waze-on-cluster/` | the Waze tool 0.7.3, as published there (`waze-on-cluster@0.7.3.tgz`, sha256 `990dfe22…`) |
| `source/` | the two tools' source at that commit (`make target` builds them in Docker) |

The tools need the Store's deploy tool 0.7.0 or newer (the Waze tool's activate and
deactivate hooks), which the Store installs first.

GPL-3.0-or-later (`LICENSE`); cluster-render's client parts are MPL-2.0
(`cluster-render/LICENSES`). Details in `source/*/README.md`.
