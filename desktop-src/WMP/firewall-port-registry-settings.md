---
title: Registro de porta de firewall Configurações
description: Registro de porta de firewall Configurações
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player,configurações do registro de porta do firewall
- Windows Media Player, configurações do registro de porta
- Windows Media Player, registro
- registro, configurações de porta de firewall
- registro, configurações de porta
- registry,settings for Windows Media Player
- configurações do registro de porta do firewall
- configurações do registro de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140f55a4008a03c2b3bc4184e2eca92129a5e30dc69f0871da856b4555daec73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576763"
---
# <a name="firewall-port-registry-settings"></a>Registro de porta de firewall Configurações

Windows Media Player coloca entradas no Registro para que os firewalls possam determinar se as portas usadas pelo compartilhamento de biblioteca de mídia devem ser abertas ou fechar.

**Entrada do Registro AcceptedEULA**

Windows Media Player usa a seguinte entrada do Registro para indicar se o usuário aceitou o EULA (Contrato de Licença do Usuário Final).


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



Um valor de 1 indica que o usuário aceitou o contrato de licença. Um valor de 0 indica que o usuário não aceitou o contrato de licença.

**WMPNSSFirewallPortsA abrir entrada do Registro**

Windows Media Player usa a seguinte entrada do Registro para indicar se o usuário optou por compartilhar sua biblioteca de mídia com outros computadores em uma rede base.


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



Um valor de 1 indica que o usuário optou por compartilhar a biblioteca. Um valor de 0 indica que o usuário optou por não compartilhar a biblioteca.

**Portas relacionadas ao compartilhamento da biblioteca de mídia**

No Windows Vista, se a entrada do Registro **WMPNSSFirewallPortsOpen** tiver um valor de 1, as portas a seguir deverão ser abertas.



| Porta          | Protocolo                  | Processo                         | Direção            |
|---------------|---------------------------|---------------------------------|----------------------|
| 554           | TCP RTSP                  | wmpnetwk.exe                    | entrada e saída |
| 8554 - 8558   | TCP RTSP                  | wmpnetwk.exe                    | entrada e saída |
| 5004, 5005    | UDP RTCP/RTP              | wmpnetwk.exe                    | entrada e saída |
| 50004 - 50013 | UDP RTCP/RTP              | wmpnetwk.exe                    | entrada e saída |
| 1900          | UDP SSDP                  | SSDPsrv em svchost.exe          | entrada e saída |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost no svchost.exe | entrada              |
| 10280 - 10284 | Registro UDP WMDRM-ND | wmpnetwk.exe                    | entrada e saída |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | entrada              |
| 2177          | TCP UDP qWAVE             | svchost.exe                     | entrada e saída |



 

No Windows Vista, se a entrada do Registro **AcceptedEULA** tiver um valor de 1, as portas a seguir deverão ser abertas.



| Porta          | Protocolo       | Processo                         | Direção            |
|---------------|----------------|---------------------------------|----------------------|
| Todas as portas UDP | UDP RTP, MSB   | wmplayer.exe, qualquer sub-rede        | entrada              |
| 1900          | UDP SSDP       | SSDPsrv/UPnPHost no svchost.exe | entrada e saída |
| 2869          | TCP SSDP, UPnP | SSDPsrv, UPnPHost               | entrada              |



 

No Microsoft Windows XP, se a entrada do Registro **WMPNSSFirewallPortsA abrir** tiver um valor de 1, as portas a seguir deverão estar abertas.



| Porta          | Protocolo                  | Processo                         | Direção            |
|---------------|---------------------------|---------------------------------|----------------------|
| 1900          | UDP SSDP                  | SSDPsrv em svchost.exe          | entrada e saída |
| 2869          | TCP SSDP, UPnP            | SSDPsrv/UPnPHost no svchost.exe | entrada              |
| 10280 - 10284 | Registro UDP WMDRM-ND | wmpnetwk.exe                    | entrada e saída |
| 10243         | TCP HTTP                  | wmpnetwk.exe                    | entrada              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> </dl>

 

 




