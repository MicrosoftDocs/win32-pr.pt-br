---
title: O que há de novo no WinRM 2,0
description: Novos recursos estão disponíveis na versão Gerenciamento Remoto do Windows 2,0. (WinRM 2,0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54f4a4829bffdb816854de2a3ebe98106a5a65af
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365659"
---
# <a name="whats-new-in-winrm-20"></a>O que há de novo no WinRM 2,0

Novos recursos estão disponíveis na versão Gerenciamento Remoto do Windows 2,0. (WinRM 2,0)

O WinRM 2,0 está incluído no Windows Server 2008 R2 e no Windows 7.

Você também pode baixar o WinRM 2,0 para Windows Server 2008 com Service Pack 2 (SP2) e Windows Vista com Service Pack 2 (SP2). Para obter informações sobre como baixar o WinRM 2,0, consulte [KB968929](https://support.microsoft.com/kb/968929).

A tabela a seguir lista a documentação do WinRM 2,0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="client-shell-api.md">API do shell do cliente WinRM</a><br/></td>
<td>A API (interface de programação de aplicativo) do Shell de cliente WinRM fornece funcionalidade para criar e gerenciar shells e operações de Shell, comandos e fluxos de dados em computadores remotos. <br/></td>
</tr>
<tr class="even">
<td><a href="winrm-plugin-api.md">API de plug-in do WinRM</a><br/></td>
<td>A API de plug-in do WinRM fornece funcionalidade que permite que um usuário grave plug-ins implementando determinadas APIs para operações e <a href="windows-remote-management-glossary.md"><em>URIs de recursos</em></a> com suporte.<br/></td>
</tr>
<tr class="odd">
<td><a href="winrm-application-hosting.md">Infraestrutura para gerenciar serviços hospedados</a><br/></td>
<td>O WinRM 2,0 apresenta uma estrutura de hospedagem. Há suporte para dois modelos de hospedagem. Um é baseado no serviço de informações da Internet (IIS) e o outro é o WinRM – baseado em serviço. <br/> Para obter mais informações sobre a configuração do host, consulte os seguintes tópicos:<br/>
<ul>
<li><a href="iis-host-plug-in-configuration.md">Configuração de plug-in de host do IIS</a></li>
<li><a href="wsman-service-plug-in-configuration.md">Configuração de plug-in do serviço WinRM</a></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="dmtf-association-traversal.md">Descoberta de perfil de DMTF por meio de passagem de associação</a><br/></td>
<td>A passagem de associação permite que um usuário recupere instâncias de classes de associação usando um mecanismo de filtragem padrão.<br/></td>
</tr>
<tr class="odd">
<td><a href="remote-shell-infrastructure-improvements.md">Aprimoramentos na infraestrutura do shell remoto</a><br/></td>
<td>Este tópico inclui informações sobre as melhorias de infraestrutura remota para o WinRM. <br/></td>
</tr>
<tr class="even">
<td><a href="multi-hop-support.md">Suporte a vários saltos</a><br/></td>
<td>A funcionalidade foi adicionada ao WinRM 2,0 que dá suporte à delegação de credenciais de usuário em vários computadores remotos. <br/> O tópico de <a href="authentication-constants.md"><strong>constantes de autenticação</strong></a> foi atualizado para adicionar a seguinte constante: <strong>WSManFlagUseCredSsp</strong>.<br/> A seguinte API C++ foi adicionada para fornecer suporte a vários saltos: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.<br/> A API de script a seguir foi adicionada para fornecer suporte a vários saltos: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="quotas.md">Gerenciamento de cota para shells remotos</a><br/></td>
<td>Este tópico inclui informações sobre a configuração de cota para gerenciamento remoto de Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="winrm-powershell-commandlets.md">Referência gerenciada para comandos WS-Management PowerShell</a><br/></td>
<td>Os usuários do WinRM 2,0 podem usar os cmdlets do Windows PowerShell para gerenciamento do sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 





