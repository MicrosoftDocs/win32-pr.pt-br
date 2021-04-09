---
description: O Winlogon e a GINA devem comunicar informações de inicialização, lidar com monitoramento e notificação de sequência de atenção segura (SAS) e permitir atividades de logoff e desligamento.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: 'Interação entre Winlogon e GINA '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759d9171bca02e0a00fd35b77a4514d7438d43f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011627"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interação entre Winlogon e GINA 

O [*Winlogon*](../secgloss/w-gly.md) e a [*Gina*](../secgloss/g-gly.md) devem comunicar informações de inicialização, lidar com monitoramento e notificação de [*sequência de atenção segura*](../secgloss/s-gly.md) (SAS) e permitir atividades de logoff e desligamento. O estado do Winlogon determina qual função GINA é chamada para processar qualquer evento SAS específico. As comunicações ocorrem na ordem mostrada aqui.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Inicialização da estação de trabalho</td>
<td><ol>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> da Gina para notificar a Gina sobre a versão do Winlogon em uso.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> da Gina para dar ao Gina os endereços das funções de suporte, um identificador para o Winlogon e obter as informações de <a href="/windows/desktop/SecGloss/c-gly"><em>contexto</em></a> para a Gina (a ser usada em todas as chamadas futuras para a Gina).<br/> O Winlogon está no estado de logoff.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Ninguém está conectado</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>O GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> do Winlogon quando um evento SAS foi recebido.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> da Gina, permitindo que a Gina processe a identificação de um usuário e as informações de autenticação.<br/> Quando o logon for bem-sucedido, o Winlogon estará no estado conectado.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>O usuário está conectado</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>O GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> do Winlogon quando um evento SAS foi recebido.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina, permitindo que a Gina apresente opções ao usuário que está conectado no momento.</li>
</ol></td>
</tr>
<tr class="even">
<td>O usuário está conectado e deseja bloquear o computador</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</li>
<li>A GINA retorna WLX_SAS_ACTION_LOCK_WKSTA.<br/> O Winlogon está no estado bloqueado da estação de trabalho.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>O usuário está conectado, a estação de trabalho está bloqueada e o usuário deseja desbloquear o computador</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> da Gina.</li>
<li>A GINA retorna WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>O usuário está conectado e o programa chama a função <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></td>
<td>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</td>
</tr>
<tr class="odd">
<td>O usuário está conectado e deseja fazer logoff usando SAS</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</li>
<li>A GINA retorna WLX_SAS_ACTION_LOGOFF.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</li>
</ol></td>
</tr>
<tr class="even">
<td>O usuário está conectado e deseja fazer logoff e desligar usando o <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></td>
<td><ol>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> da Gina.</li>
</ol></td>
</tr>
<tr class="odd">
<td>O usuário está conectado e deseja fazer logoff e desligar usando SAS</td>
<td>(A GINA monitora os dispositivos em busca de eventos de SAS).
<ol>
<li>A GINA chama a função <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> da Gina.</li>
<li>A GINA retorna WLX_SAS_ACTION_SHUTDOWN.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> da Gina.</li>
<li>O Winlogon chama a função <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> da Gina.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
