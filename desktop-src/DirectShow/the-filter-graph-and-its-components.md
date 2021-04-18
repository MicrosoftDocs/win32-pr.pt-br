---
description: O gráfico de filtro e seus componentes
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: O gráfico de filtro e seus componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812970"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="48d8b-103">O gráfico de filtro e seus componentes</span><span class="sxs-lookup"><span data-stu-id="48d8b-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="48d8b-104">Este artigo descreve os principais componentes do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="48d8b-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="48d8b-105">Ele é destinado a uma introdução para desenvolvedores de aplicativos e desenvolvedores que escrevem filtros DirectShow personalizados.</span><span class="sxs-lookup"><span data-stu-id="48d8b-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="48d8b-106">Os desenvolvedores de aplicativos geralmente podem ignorar muitos dos detalhes de baixo nível do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="48d8b-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="48d8b-107">No entanto, ainda é uma boa ideia ler esta seção para ter uma compreensão geral da arquitetura do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="48d8b-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="48d8b-108">Este artigo inclui as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="48d8b-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="48d8b-109">Sobre filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="48d8b-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="48d8b-110">Sobre o Gerenciador do grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="48d8b-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="48d8b-111">Sobre os tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="48d8b-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="48d8b-112">Sobre exemplos de mídia e alocadores</span><span class="sxs-lookup"><span data-stu-id="48d8b-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="48d8b-113">Como os dispositivos de hardware participam do grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="48d8b-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



