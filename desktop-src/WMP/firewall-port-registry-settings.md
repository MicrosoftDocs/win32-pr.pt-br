---
title: Configurações do registro de porta do firewall
description: Configurações do registro de porta do firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, configurações do registro de porta do firewall
- Windows Media Player, configurações do registro de porta
- Windows Media Player, registro
- configurações de porta do registro, firewall
- registro, configurações de porta
- registro, configurações do Windows Media Player
- configurações do registro de porta do firewall
- configurações do registro de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822342"
---
# <a name="firewall-port-registry-settings"></a>Configurações do registro de porta do firewall

O Windows Media Player coloca entradas no registro para que os firewalls possam determinar se devem ser abertas ou fechadas as portas usadas pelo compartilhamento de biblioteca de mídia.

**Entrada do registro AcceptedEULA**

O Windows Media Player usa a seguinte entrada de registro para indicar se o usuário aceitou o EULA (contrato de licença de usuário final).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Um valor de 1 indica que o usuário aceitou o contrato de licença. Um valor de 0 indica que o usuário não aceitou o contrato de licença.

**Entrada do registro WMPNSSFirewallPortsOpen**

O Windows Media Player usa a seguinte entrada de registro para indicar se o usuário optou por compartilhar sua biblioteca de mídias com outros computadores em uma rede doméstica.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Um valor de 1 indica que o usuário optou por compartilhar a biblioteca. Um valor de 0 indica que o usuário optou por não compartilhar a biblioteca.

**Portas relacionadas ao compartilhamento de biblioteca de mídia**

No Windows Vista, se a entrada do registro **WMPNSSFirewallPortsOpen** tiver um valor de 1, as portas a seguir deverão ser abertas.



| Porta          | Protocolo                  | Processar                         | Direção            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | RTSP TCP                  | wmpnetwk.exe                    | entrada e saída |
| 8554-8558   | RTSP TCP                  | wmpnetwk.exe                    | entrada e saída |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | entrada e saída |
| 50004-50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | entrada e saída |
| 1900          | SSDP UDP                  | SSDPsrv em svchost.exe          | entrada e saída |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost no svchost.exe | entrada              |
| 10280-10284 | Registro de WMDRM-ND de UDP | wmpnetwk.exe                    | entrada e saída |
| 10243         | HTTP TCP                  | wmpnetwk.exe                    | entrada              |
| 2177          | QWAVE TCP UDP             | svchost.exe                     | entrada e saída |



 

No Windows Vista, se a entrada do registro **AcceptedEULA** tiver um valor de 1, as portas a seguir deverão ser abertas.



| Porta          | Protocolo       | Processar                         | Direção            |
|---------------|----------------|---------------------------------|----------------------|
| Todas as portas UDP | UDP RTP, MSB   | wmplayer.exe, qualquer sub-rede        | entrada              |
| 1900          | SSDP UDP       | SSDPsrv/UPnPHost no svchost.exe | entrada e saída |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | entrada              |



 

No Microsoft Windows XP, se a entrada do registro **WMPNSSFirewallPortsOpen** tiver um valor de 1, as portas a seguir deverão ser abertas.



| Porta          | Protocolo                  | Processar                         | Direção            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | SSDP UDP                  | SSDPsrv em svchost.exe          | entrada e saída |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost no svchost.exe | entrada              |
| 10280-10284 | Registro de WMDRM-ND de UDP | wmpnetwk.exe                    | entrada e saída |
| 10243         | HTTP TCP                  | wmpnetwk.exe                    | entrada              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> </dl>

 

 




