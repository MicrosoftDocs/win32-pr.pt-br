---
title: Sobre o Gerenciador de tabela de roteamento versão 2
description: A documentação a seguir descreve a tecnologia de Gerenciador de tabela de roteamento versão 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2, descrito
- Gerenciador de tabela de roteamento versão 2 RRAS
- Gerenciador de tabela de roteamento versão 2 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005640"
---
# <a name="about-routing-table-manager-version-2"></a><span data-ttu-id="bd351-107">Sobre o Gerenciador de tabela de roteamento versão 2</span><span class="sxs-lookup"><span data-stu-id="bd351-107">About Routing Table Manager Version 2</span></span>

<span data-ttu-id="bd351-108">A documentação a seguir descreve a tecnologia de Gerenciador de tabela de roteamento versão 2 (RTMv2).</span><span class="sxs-lookup"><span data-stu-id="bd351-108">The following documentation describes the Routing Table Manager Version 2 (RTMv2) technology.</span></span> <span data-ttu-id="bd351-109">A API do RTMv2 é um recurso do Windows 2000 e sistemas operacionais posteriores que você pode usar para gravar protocolos de roteamento que interagem com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="bd351-109">The RTMv2 API is a feature of Windows 2000 and later operating systems that you can use to write routing protocols that interact with the routing table manager.</span></span>

<span data-ttu-id="bd351-110">O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="bd351-110">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span>

<span data-ttu-id="bd351-111">O RTMv2 não está disponível para o Windows NT versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="bd351-111">RTMv2 is not available for Windows NT version 4.0.</span></span> <span data-ttu-id="bd351-112">Além disso, o RTMv2 não pode ser usado para protocolos de roteamento IPX que são executados no Windows NT 4,0 ou no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bd351-112">Additionally, RTMv2 cannot be used for IPX routing protocols that run on Windows NT 4.0 or Windows 2000.</span></span> <span data-ttu-id="bd351-113">Se você estiver usando IPX ou gravando protocolos de roteamento para o Windows NT 4,0, consulte [sobre o Gerenciador de tabela de roteamento versão 1](about-routing-table-manager-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="bd351-113">If you are using IPX or writing routing protocols for Windows NT 4.0, please refer to [About Routing Table Manager Version 1](about-routing-table-manager-version-1.md).</span></span>

<span data-ttu-id="bd351-114">Esta visão geral descreve os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="bd351-114">This overview describes the following topics:</span></span>

-   [<span data-ttu-id="bd351-115">Componentes da arquitetura do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bd351-115">Components of the Routing Table Manager Architecture</span></span>](components-of-the-routing-table-manager-architecture.md)
-   [<span data-ttu-id="bd351-116">Registrando com o Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bd351-116">Registering with the Routing Table Manager</span></span>](registering-with-the-routing-table-manager.md)
-   [<span data-ttu-id="bd351-117">Enumerando entidades registradas</span><span class="sxs-lookup"><span data-stu-id="bd351-117">Enumerating Registered Entities</span></span>](enumerating-registered-entities.md)
-   [<span data-ttu-id="bd351-118">Usando métodos</span><span class="sxs-lookup"><span data-stu-id="bd351-118">Using Methods</span></span>](using-methods.md)
-   [<span data-ttu-id="bd351-119">Usando ponteiros opacos</span><span class="sxs-lookup"><span data-stu-id="bd351-119">Using Opaque Pointers</span></span>](using-opaque-pointers.md)
-   [<span data-ttu-id="bd351-120">Marcando rotas para o estado de Hold-Down</span><span class="sxs-lookup"><span data-stu-id="bd351-120">Marking Routes for the Hold-Down State</span></span>](marking-routes-for-the-hold-down-state.md)
-   [<span data-ttu-id="bd351-121">Adicionando rotas</span><span class="sxs-lookup"><span data-stu-id="bd351-121">Adding Routes</span></span>](adding-routes.md)
-   [<span data-ttu-id="bd351-122">Recuperando informações de rota</span><span class="sxs-lookup"><span data-stu-id="bd351-122">Retrieving Route Information</span></span>](retrieving-route-information.md)
-   [<span data-ttu-id="bd351-123">Atualizando rotas</span><span class="sxs-lookup"><span data-stu-id="bd351-123">Updating Routes</span></span>](updating-routes.md)
-   [<span data-ttu-id="bd351-124">Recebendo notificação de alterações</span><span class="sxs-lookup"><span data-stu-id="bd351-124">Receiving Notification of Changes</span></span>](receiving-notification-of-changes.md)
-   [<span data-ttu-id="bd351-125">Trabalhando com próximos saltos</span><span class="sxs-lookup"><span data-stu-id="bd351-125">Working with Next Hops</span></span>](working-with-next-hops.md)
-   [<span data-ttu-id="bd351-126">Enumerando entradas da tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bd351-126">Enumerating Routing Table Entries</span></span>](enumerating-routing-table-entries.md)
-   [<span data-ttu-id="bd351-127">Localizando informações específicas na tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bd351-127">Finding Specific Information in the Routing Table</span></span>](finding-specific-information-in-the-routing-table.md)
-   [<span data-ttu-id="bd351-128">Manutenção de listas de Client-Specific</span><span class="sxs-lookup"><span data-stu-id="bd351-128">Maintaining Client-Specific Lists</span></span>](maintaining-client-specific-lists.md)
-   [<span data-ttu-id="bd351-129">Gerenciando identificadores</span><span class="sxs-lookup"><span data-stu-id="bd351-129">Managing Handles</span></span>](managing-handles.md)

 

 




