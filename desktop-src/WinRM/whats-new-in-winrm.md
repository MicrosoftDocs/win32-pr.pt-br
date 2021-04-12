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
# <a name="whats-new-in-winrm-20"></a><span data-ttu-id="b59b3-104">O que há de novo no WinRM 2,0</span><span class="sxs-lookup"><span data-stu-id="b59b3-104">What's New in WinRM 2.0</span></span>

<span data-ttu-id="b59b3-105">Novos recursos estão disponíveis na versão Gerenciamento Remoto do Windows 2,0.</span><span class="sxs-lookup"><span data-stu-id="b59b3-105">New features are available in Windows Remote Management version 2.0.</span></span> <span data-ttu-id="b59b3-106">(WinRM 2,0)</span><span class="sxs-lookup"><span data-stu-id="b59b3-106">(WinRM 2.0)</span></span>

<span data-ttu-id="b59b3-107">O WinRM 2,0 está incluído no Windows Server 2008 R2 e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b59b3-107">WinRM 2.0 is included in Windows Server 2008 R2 and Windows 7.</span></span>

<span data-ttu-id="b59b3-108">Você também pode baixar o WinRM 2,0 para Windows Server 2008 com Service Pack 2 (SP2) e Windows Vista com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="b59b3-108">You can also download WinRM 2.0 for Windows Server 2008 with Service Pack 2 (SP2) and Windows Vista with Service Pack 2 (SP2).</span></span> <span data-ttu-id="b59b3-109">Para obter informações sobre como baixar o WinRM 2,0, consulte [KB968929](https://support.microsoft.com/kb/968929).</span><span class="sxs-lookup"><span data-stu-id="b59b3-109">For information about downloading WinRM 2.0, see [KB968929](https://support.microsoft.com/kb/968929).</span></span>

<span data-ttu-id="b59b3-110">A tabela a seguir lista a documentação do WinRM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b59b3-110">The following table lists the documentation for WinRM 2.0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b59b3-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="b59b3-111">Topic</span></span></th>
<th><span data-ttu-id="b59b3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b59b3-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b59b3-113"><a href="client-shell-api.md">API do shell do cliente WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-113"><a href="client-shell-api.md">WinRM Client Shell API</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-114">A API (interface de programação de aplicativo) do Shell de cliente WinRM fornece funcionalidade para criar e gerenciar shells e operações de Shell, comandos e fluxos de dados em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="b59b3-114">The WinRM Client Shell application programming interface (API) provides functionality to create and manage shells and shell operations, commands, and data streams on remote computers.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b59b3-115"><a href="winrm-plugin-api.md">API de plug-in do WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-115"><a href="winrm-plugin-api.md">WinRM Plugin API</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-116">A API de plug-in do WinRM fornece funcionalidade que permite que um usuário grave plug-ins implementando determinadas APIs para operações e <a href="windows-remote-management-glossary.md"><em>URIs de recursos</em></a> com suporte.</span><span class="sxs-lookup"><span data-stu-id="b59b3-116">The WinRM Plug-in API provides functionality that enables a user to write plug-ins by implementing certain APIs for supported <a href="windows-remote-management-glossary.md"><em>resource URIs</em></a> and operations.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b59b3-117"><a href="winrm-application-hosting.md">Infraestrutura para gerenciar serviços hospedados</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-117"><a href="winrm-application-hosting.md">Infrastructure for Managing Hosted Services</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-118">O WinRM 2,0 apresenta uma estrutura de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="b59b3-118">WinRM 2.0 introduces a hosting framework.</span></span> <span data-ttu-id="b59b3-119">Há suporte para dois modelos de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="b59b3-119">Two hosting models are supported.</span></span> <span data-ttu-id="b59b3-120">Um é baseado no serviço de informações da Internet (IIS) e o outro é o WinRM – baseado em serviço.</span><span class="sxs-lookup"><span data-stu-id="b59b3-120">One is Internet Information Service (IIS)–based and the other is WinRM–service based.</span></span> <br/> <span data-ttu-id="b59b3-121">Para obter mais informações sobre a configuração do host, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="b59b3-121">For more information about the host configuration, see the following topics:</span></span><br/>
<ul>
<li><span data-ttu-id="b59b3-122"><a href="iis-host-plug-in-configuration.md">Configuração de plug-in de host do IIS</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-122"><a href="iis-host-plug-in-configuration.md">IIS Host Plug-in Configuration</a></span></span></li>
<li><span data-ttu-id="b59b3-123"><a href="wsman-service-plug-in-configuration.md">Configuração de plug-in do serviço WinRM</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-123"><a href="wsman-service-plug-in-configuration.md">WinRM Service Plug-in Configuration</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b59b3-124"><a href="dmtf-association-traversal.md">Descoberta de perfil de DMTF por meio de passagem de associação</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-124"><a href="dmtf-association-traversal.md">DMTF Profile Discovery through Association Traversal</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-125">A passagem de associação permite que um usuário recupere instâncias de classes de associação usando um mecanismo de filtragem padrão.</span><span class="sxs-lookup"><span data-stu-id="b59b3-125">Association traversal enables a user to retrieve instances of Association classes by using a standard filtering mechanism.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b59b3-126"><a href="remote-shell-infrastructure-improvements.md">Aprimoramentos na infraestrutura do shell remoto</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-126"><a href="remote-shell-infrastructure-improvements.md">Remote Shell infrastructure improvements</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-127">Este tópico inclui informações sobre as melhorias de infraestrutura remota para o WinRM.</span><span class="sxs-lookup"><span data-stu-id="b59b3-127">This topic includes information about the remote infrastructure improvements for WinRM.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b59b3-128"><a href="multi-hop-support.md">Suporte a vários saltos</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-128"><a href="multi-hop-support.md">Multi-hop Support</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-129">A funcionalidade foi adicionada ao WinRM 2,0 que dá suporte à delegação de credenciais de usuário em vários computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="b59b3-129">Functionality was added to WinRM 2.0 that supports delegating user credentials across multiple remote computers.</span></span> <br/> <span data-ttu-id="b59b3-130">O tópico de <a href="authentication-constants.md"><strong>constantes de autenticação</strong></a> foi atualizado para adicionar a seguinte constante: <strong>WSManFlagUseCredSsp</strong>.</span><span class="sxs-lookup"><span data-stu-id="b59b3-130">The <a href="authentication-constants.md"><strong>Authentication Constants</strong></a> topic was updated to add the following constant: <strong>WSManFlagUseCredSsp</strong>.</span></span><br/> <span data-ttu-id="b59b3-131">A seguinte API C++ foi adicionada para fornecer suporte a vários saltos: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b59b3-131">The following C++ API was added to provide multi-hop support: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3</strong></a>.</span></span><br/> <span data-ttu-id="b59b3-132">A API de script a seguir foi adicionada para fornecer suporte a vários saltos: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan. SessionFlagUseCredSsp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b59b3-132">The following scripting API was added to provide multi-hop support: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b59b3-133"><a href="quotas.md">Gerenciamento de cota para shells remotos</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-133"><a href="quotas.md">Quota Management for Remote Shells</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-134">Este tópico inclui informações sobre a configuração de cota para gerenciamento remoto de Shell.</span><span class="sxs-lookup"><span data-stu-id="b59b3-134">This topic includes information about quota configuration for remote shell management.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b59b3-135"><a href="winrm-powershell-commandlets.md">Referência gerenciada para comandos WS-Management PowerShell</a></span><span class="sxs-lookup"><span data-stu-id="b59b3-135"><a href="winrm-powershell-commandlets.md">Managed Reference for WS-Management PowerShell Commands</a></span></span><br/></td>
<td><span data-ttu-id="b59b3-136">Os usuários do WinRM 2,0 podem usar os cmdlets do Windows PowerShell para gerenciamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="b59b3-136">Users of WinRM 2.0 can use Windows PowerShell cmdlets for system management.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





