# dashmachine
DashMachine - Dashboard Apps - Docker compose

Ver en "localhost:8200"

Username: admin

Password: admin


# Modificar el Dashboard:

Desplace el cursor sobre la barra lateral izquierda y haga clic en el engranaje Configuración.

Su archivo Config.ini se verá así:

[Settings]
theme = light
accent = orange
background = None
roles = admin,user,public_user
home_access_groups = admin_only
settings_access_groups = admin_only
custom_app_title = DashMachine

Las primeras cosas que cambié fueron el tema y el acento a "oscuro" y "azul" respectivamente:

[Settings]
theme = dark
accent = blue
background = None
roles = admin,user,public_user
home_access_groups = admin_only
settings_access_groups = admin_only
custom_app_title = DashMachine

Debido a que tengo varias aplicaciones/contenedores en mi servidor, quería que todos fueran accesibles, así que aquí hay un ejemplo de un par de configuraciones de enlaces de aplicaciones en mi DashMachine Config.ini:

[Emby]
prefix = http://
url = 192.168.1.19:8096/web
icon = static/images/apps/emby.png
sidebar_icon = static/images/apps/emby.png
description = Emby Media Server
open_in = new_tab

[PiHole]
prefix = http://
url = 192.168.1.225/admin
icon = static/images/apps/pihole.png
sidebar_icon = static/images/apps/pihole.png
description = DNS Ad Blocker
open_in = new_tab
