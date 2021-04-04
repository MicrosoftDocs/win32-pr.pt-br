---
title: O que há de novo no Windows Server 2008 R2
description: O Windows Server 2008 R2 apresenta os seguintes novos elementos de programação para Serviços de Área de Trabalho Remota.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103916946"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="fbc74-103">O que há de novo no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbc74-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="fbc74-104">O Windows Server 2008 R2 apresenta os seguintes novos elementos de programação para Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="fbc74-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbc74-105">Os serviços de terminal agora estão Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="fbc74-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="fbc74-106">Os serviços de terminal foram renomeados Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="fbc74-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="fbc74-107">Um servidor com o serviço de função Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) instalado agora é chamado de servidor Host da Sessão RD, em vez de um servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="fbc74-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="fbc74-108"><a href="terminal-services-is-now-remote-desktop-services.md">Os serviços de terminal agora estão Serviços de Área de Trabalho Remota</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbc74-109">API de virtualização Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="fbc74-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="fbc74-110">A API de virtualização Área de Trabalho Remota fornece enumerações, interfaces e estruturas que você pode usar para criar plug-ins personalizados que substituem a lógica de redirecionamento padrão do Conexão de Área de Trabalho Remota Broker (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="fbc74-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="fbc74-111">O agente de conexão RD (anteriormente conhecido como agente de Sessão TS) foi expandido para dar suporte a conexões com máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="fbc74-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="fbc74-112"><a href="using-the-remote-desktop-virtualization-api.md">Usando a API de virtualização Área de Trabalho Remota</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="fbc74-113"><a href="terminal-services-virtualization-api-reference.md">Referência de API de virtualização Área de Trabalho Remota</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbc74-114">Provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="fbc74-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="fbc74-115">A API do provedor de protocolo RDP pode ser usada para criar um protocolo que personaliza a interação entre o serviço Serviços de Área de Trabalho Remota e os clientes da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fbc74-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="fbc74-116"><a href="creating-a-custom-remote-protocol.md">Criando um provedor de protocolo RDP</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="fbc74-117"><a href="custom-remote-protocol-reference.md">Referência do provedor de protocolo RDP</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbc74-118">API do AudioEndpoint Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="fbc74-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="fbc74-119">O Serviços de Área de Trabalho Remota API AudioEndpoint dá suporte à enumeração, interfaces e estruturas para registro de ponto de extremidade de áudio e transporte de dados.</span><span class="sxs-lookup"><span data-stu-id="fbc74-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="fbc74-120"><a href="terminal-services-audioendpoint-api-reference.md">Serviços de Área de Trabalho Remota referência da API AudioEndpoint</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbc74-121">API de Serviço Gerenciamento de Conexão de RemoteApp e Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="fbc74-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="fbc74-122">A API do Serviço Gerenciamento de Conexão de RemoteApp e Área de Trabalho dá suporte a interfaces e estruturas que você pode usar para executar a filtragem personalizada de recursos e fornecer suporte para tipos de arquivos que não têm suporte nativo no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fbc74-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="fbc74-123"><a href="centralized-publishing-api-reference.md">Referência da API do Serviço Gerenciamento de Conexão de RemoteApp e Área de Trabalho</a></span><span class="sxs-lookup"><span data-stu-id="fbc74-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





