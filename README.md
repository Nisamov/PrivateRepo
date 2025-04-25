# Secure Service Protocol
Este software permite controlar el estado de los servicios en tu equipo Debian.
Puede ser peligroso si se configura de una mala manera.

## Instalación
Para instalarlo asegúrate de haberte descargado el fichero `.deb`del repositorio.
Tras descargarlo, ubicate en la ruta del fichero y ejecuta el siguiente comando:
```sh
sudo dpkg -i fichero.deb
```

## Rutas
Las rutas usadas del software son:
> /usr/local/sbin/ssp_files -> Contiene los ficheros generales del servicio.
> /etc/ssp.conf -> Contiene la configuración del servicio.
> /lib/systemd/system/ssp.service -> Servicio Secure Service Protocol

## Configuración
Para que el servicio pueda leer y aplicar la configuración establecida, es necesario reiniciar el servicio, pues este, lee durante su arranque, la configuración.
No obstante, lee activamente los ficheros de los servicios permitidos en el sistema.

## Comandos
SSP cuenta con comandos de terminal para poder administrar con mayor facilidad el servicio.

```
.
├── .github
│   └── workflows
│       └── build_deb.yml
├── DEBIAN
│   ├── control
│   ├── postint
│   └── prerm
├── etc
│   └── ssp.conf
├── lib
│   └── systemd
│       └── system
│           └── ssp.service
├── usr
│   └── local
│       └── sbin
│           ├── ssp_files
│           │   ├── LICENSE
│           │   └── service.py
│           └── ssp
├── funcionamiento.md
└── README.md
```