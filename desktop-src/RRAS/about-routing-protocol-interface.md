---
title: Sobre a interface do protocolo de roteamento
description: A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento, descrito
- Interface do protocolo de roteamento RRAS
- Interface do protocolo de roteamento RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636348"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="325e9-107">Sobre a interface do protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="325e9-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="325e9-108">A documentação a seguir descreve a integração de protocolos de roteamento de terceiros ao RRAS (serviço de roteamento e acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="325e9-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="325e9-109">O RRAS é um recurso do Windows que funciona como um roteador de vários protocolos.</span><span class="sxs-lookup"><span data-stu-id="325e9-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="325e9-110">O RRAS define a interface entre o Gerenciador de roteador e o protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="325e9-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="325e9-111">O protocolo de roteamento é implementado em uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="325e9-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="325e9-112">Use essa interface para implementar protocolos de roteamento, como IGRP, NLSP e BGP, como DLLs de modo de usuário que funcionam com o RRAS.</span><span class="sxs-lookup"><span data-stu-id="325e9-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="325e9-113">Esta documentação descreve os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="325e9-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="325e9-114">Adaptadores</span><span class="sxs-lookup"><span data-stu-id="325e9-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="325e9-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="325e9-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="325e9-116">Rotas estáticas e auto-estáticas</span><span class="sxs-lookup"><span data-stu-id="325e9-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




