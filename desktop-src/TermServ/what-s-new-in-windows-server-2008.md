---
title: O que há de novo no Windows Server 2008
description: O Windows Server 2008 apresenta os seguintes novos elementos de programação para serviços de terminal.
ms.assetid: a2299b03-5e06-4984-a33f-b44c7cded513
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab74f22c41fa88147a1ef30a8f55f158e34990c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104366815"
---
# <a name="whats-new-in-windows-server-2008"></a>O que há de novo no Windows Server 2008

O Windows Server 2008 apresenta os seguintes novos elementos de programação para serviços de terminal.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento de programação</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Referência de canais virtuais dinâmicos<br/></td>
<td>As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para serviços de terminal, conhecidas como APIs de SVC (canal virtual estático).<br/>
<ul>
<li><a href="dynamic-virtual-channels.md">Canais virtuais dinâmicos</a></li>
<li><a href="dynamic-virtual-channels-reference.md">Referência de canais virtuais dinâmicos</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Referência de Conexão Web de Área de Trabalho Remota<br/></td>
<td>As seguintes interfaces (e seus métodos e propriedades associados) foram adicionadas à <a href="remote-desktop-web-connection-reference.md">referência conexão Web de área de trabalho remota</a>:<br/>
<ul>
<li><a href="imsrdpclient5.md"><strong>Interface IMsRdpClient5</strong></a></li>
<li><a href="imsrdpclient6.md"><strong>Interface IMsRdpClient6</strong></a></li>
<li><a href="imsrdpclientadvancedsettings5.md"><strong>Interface IMsRdpClientAdvancedSettings5</strong></a></li>
<li><a href="imsrdpclientadvancedsettings6.md"><strong>Interface IMsRdpClientAdvancedSettings6</strong></a></li>
<li><a href="imsrdpclientnonscriptable3.md"><strong>Interface IMsRdpClientNonScriptable3</strong></a></li>
<li><a href="imsrdpclientshell.md"><strong>Interface IMsRdpClientShell</strong></a></li>
<li><a href="imsrdpclienttransportsettings.md"><strong>Interface IMsRdpClientTransportSettings</strong></a></li>
<li><a href="imsrdpclienttransportsettings2.md"><strong>Interface IMsRdpClientTransportSettings2</strong></a></li>
<li><a href="imsrdpdevice.md"><strong>Interface IMsRdpDevice</strong></a></li>
<li><a href="imsrdpdevicecollection.md"><strong>Interface IMsRdpDeviceCollection</strong></a></li>
<li><a href="imsrdpdrive.md"><strong>Interface IMsRdpDrive</strong></a></li>
<li><a href="imsrdpdrivecollection.md"><strong>Interface IMsRdpDriveCollection</strong></a></li>
<li><a href="itsremoteprogram.md"><strong>Interface ITSRemoteProgram</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Referência da API dos serviços de terminal<br/></td>
<td>As funções a seguir foram adicionadas à <a href="terminal-services-api-reference.md">referência da API dos serviços de terminal</a>:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona"><strong>Função WTSConnectSession</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex"><strong>Função WTSRegisterSessionNotificationEx</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona"><strong>Função WTSStartRemoteControlSession</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession"><strong>Função WTSStopRemoteControlSession</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex"><strong>Função WTSUnRegisterSessionNotificationEx</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex"><strong>Função WTSVirtualChannelOpenEx</strong></a></li>
</ul>
As seguintes estruturas foram adicionadas:<br/>
<ul>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta"><strong>Estrutura WTSCLIENT</strong></a></li>
<li><a href="/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa"><strong>Estrutura WTSINFO</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Provedor WMI de serviços de terminal<br/></td>
<td>As seguintes classes e métodos foram adicionados ao <a href="terminal-services-wmi-provider.md">provedor WMI de serviços de terminal</a>.<br/>
<ul>
<li><a href="terminal-services-gateway-classes.md">Classes de gateway de serviços de terminal (e métodos associados)</a></li>
<li><a href="terminal-services-license-server-classes.md">Classes de servidor de licença dos serviços de terminal (e métodos associados)</a></li>
<li><a href="terminal-services-remoteapp-classes.md">Classes do RemoteApp (e métodos associados)</a></li>
<li><a href="win32-tsdiscoveredlicenseserver.md"><strong>Classe Win32_TSDiscoveredLicenseServer</strong></a></li>
<li><a href="create-win32-terminal.md"><strong>Método Create da classe Win32_Terminal</strong></a></li>
<li><a href="delete-win32-terminal.md"><strong>Método Delete da classe Win32_Terminal</strong></a></li>
<li><a href="canaccesslicenseserver-win32-terminalservicesetting.md"><strong>Método CanAccessLicenseServer da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="findlicenseservers-win32-terminalservicesetting.md"><strong>Método FindLicenseServers da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getdomain-win32-terminalservicesetting.md"><strong>Método GetDomain da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getgraceperioddays-win32-terminalservicesetting.md"><strong>Método GetGracePeriodDays da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="getwinstationdrivernames-win32-terminalservicesetting.md"><strong>Método GetWinstationDriverNames da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="pinglicenseserver-win32-terminalservicesetting.md"><strong>Método PingLicenseServer da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="updatedirectconnectlicenseserver-win32-terminalservicesetting.md"><strong>Método UpdateDirectConnectLicenseServer da classe Win32_TerminalServiceSetting</strong></a></li>
<li><a href="setuserauthenticationrequired-win32-tsgeneralsetting.md"><strong>Método SetUserAuthenticationRequired da classe Win32_TSGeneralSetting</strong></a></li>
<li><a href="getcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Método GetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setcurrentredirectableaddresses-win32-tssessiondirectory.md"><strong>Método SetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="getredirectableaddresses-win32-tssessiondirectory.md"><strong>Método GetRedirectableAddresses da classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="pingsessiondirectory-win32-tssessiondirectory.md"><strong>Método PingSessionDirectory da classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setloadbalancingstate-win32-tssessiondirectory.md"><strong>Método SetLoadBalancingState da classe Win32_TSSessionDirectory</strong></a></li>
<li><a href="setserverweight-win32-tssessiondirectory.md"><strong>Método SetServerWeight da classe Win32_TSSessionDirectory</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Referência de plug-in do agente de sessão dos serviços de terminal<br/></td>
<td>O plug-in do agente de sessão dos serviços de terminal (agente de Sessão TS) é usado para estender os recursos do agente de Sessão TS.<br/>
<ul>
<li><a href="/windows/desktop/TermServ/terminal-services-virtualization-api-reference">Referência de plug-in do agente de sessão dos serviços de terminal</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

