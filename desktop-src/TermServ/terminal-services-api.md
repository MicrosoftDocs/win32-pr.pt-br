---
title: API de Serviços de Área de Trabalho Remota
description: A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822510"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="a0174-103">API de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="a0174-103">Remote Desktop Services API</span></span>

<span data-ttu-id="a0174-104">A maioria dos aplicativos é executada sem modificação em um ambiente Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) e não precisa usar a API Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="a0174-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="a0174-105">A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="a0174-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="a0174-106">A API Serviços de Área de Trabalho Remota é um conjunto de chamadas de função em Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a0174-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="a0174-107">Para criar seu aplicativo para ser executado em ambientes Serviços de Área de Trabalho Remota e não Serviços de Área de Trabalho Remota, use a vinculação dinâmica em tempo de execução para verificar a presença de Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a0174-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="a0174-108">Para obter mais informações, consulte [vinculação de tempo de execução para Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a0174-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="a0174-109">A API Serviços de Área de Trabalho Remota permite que os aplicativos executem as seguintes tarefas em um ambiente de Serviços de Área de Trabalho Remota:</span><span class="sxs-lookup"><span data-stu-id="a0174-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="a0174-110">A [Administração de serviços de área de trabalho remota](terminal-services-administration.md), como a enumeração e o gerenciamento de servidores Host da Sessão da Área de Trabalho Remota (host da Sessão RD) (anteriormente conhecidos como servidores de terminal) em um domínio ou a enumeração e o gerenciamento de sessões e processos em um servidor host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="a0174-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="a0174-111">Aprimorando aplicativos cliente/servidor em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="a0174-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="a0174-112">Usar [serviços de área de trabalho remota canais virtuais](terminal-services-virtual-channels.md) para se comunicar entre módulos de cliente e de servidor de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a0174-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="a0174-113">[Definir e recuperar serviços de área de trabalho remota informações específicas de configuração do usuário](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a0174-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




