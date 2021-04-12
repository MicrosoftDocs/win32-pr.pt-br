---
title: Funções do Windows Defender
description: Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365485"
---
# <a name="windows-defender-functions"></a>Funções do Windows Defender

Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações do Windows Defender.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></td>
<td>Retorna uma mensagem de erro formatada com base em um código de erro.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></td>
<td>Libera memória para o Gerenciador de proteção contra malware.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></td>
<td>Fecha o identificador retornado por <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></td>
<td>Estabelece uma conexão com o Malware Protection Manager no computador local.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></td>
<td><strong>Sem suporte.</strong> Retorna informações de status sobre vários componentes do Malware Protection Manager.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></td>
<td>Retorna informações de status sobre vários componentes do Malware Protection Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></td>
<td>Retorna informações de versão sobre vários componentes do Gerenciador de proteção contra malware.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></td>
<td>Permite o controle de uma verificação que foi iniciada de forma assíncrona via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>MpScanStart</strong></a></td>
<td>Inicia uma operação de verificação.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></td>
<td>Retorna informações sobre a próxima ameaça na lista de enumeração. Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></td>
<td>Retorna um identificador de enumeração para a finalidade de recuperar ameaças. Essa função pode ser usada para abrir ameaças detectadas por uma verificação específica, todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou todas as ameaças presentes no banco de dados de assinatura.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></td>
<td>Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></td>
<td>Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></td>
<td>Inicia uma operação de atualização de assinatura.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></td>
<td>Altera o status do Windows Defender para ativado ou desativado.<br/>
<blockquote>
[!Note]<br />
A partir do Windows 10, versão 1607 e Windows Server 2016, a função <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> sempre retorna <strong>E_NOTIMPL</strong>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></td>
<td>Retorna o status atual do Windows Defender.<br/></td>
</tr>
</tbody>
</table>



 

 

 





