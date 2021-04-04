---
title: Arquitetura do Gerenciador de lista de rede
description: Arquitetura do Gerenciador de lista de rede
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916629"
---
# <a name="network-list-manager-architecture"></a><span data-ttu-id="9ca9e-103">Arquitetura do Gerenciador de lista de rede</span><span class="sxs-lookup"><span data-stu-id="9ca9e-103">Network List Manager Architecture</span></span>

<span data-ttu-id="9ca9e-104">O Gerenciador de lista de rede é executado como um serviço no contexto de Svchost.exe e é iniciado durante o procedimento de inicialização do computador.</span><span class="sxs-lookup"><span data-stu-id="9ca9e-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="9ca9e-105">O serviço Gerenciador de listas de rede mantém uma tabela de redes disponíveis e atributos de rede que são recuperados por aplicativos por meio da API do Gerenciador de listas de rede.</span><span class="sxs-lookup"><span data-stu-id="9ca9e-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="9ca9e-106">O Gerenciador de lista de rede fornece funções básicas para filtrar e consultar o serviço Gerenciador de listas de rede para redes específicas e recuperar os atributos dessas redes.</span><span class="sxs-lookup"><span data-stu-id="9ca9e-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="9ca9e-107">O diagrama a seguir mostra a arquitetura do Gerenciador de lista de rede e a interação entre o serviço Gerenciador de lista de rede e o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="9ca9e-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![diagrama da arquitetura de reconhecimento de rede](images/architecture.png)

 

 




