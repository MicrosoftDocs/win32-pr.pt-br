---
description: Enumerando objetos em um grafo de filtro
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Enumerando objetos em um grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087568"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="a6e9b-103">Enumerando objetos em um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="a6e9b-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="a6e9b-104">Um aplicativo pode precisar localizar um filtro específico no grafo de filtro ou até mesmo um PIN específico em um filtro.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="a6e9b-105">Por exemplo, ele pode usar uma interface que um filtro específico expõe.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="a6e9b-106">Ou, ele pode construir um grafo de filtro especializado e precisa chamar métodos em Pins individuais para conectar os filtros.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="a6e9b-107">Para essa finalidade, o DirectShow fornece vários métodos para enumerar objetos em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="a6e9b-108">Os enumeradores abordados nesta seção seguem o formulário padrão usado pelas interfaces de enumeração COM.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="a6e9b-109">Para obter mais informações, consulte o tópico "IEnumXXXX" no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="a6e9b-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="a6e9b-110">Para obter informações sobre como enumerar filtros registrados no computador do usuário, mas ainda não estão no grafo de filtro, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a6e9b-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="a6e9b-111">Este artigo contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a6e9b-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="a6e9b-112">Enumerando filtros</span><span class="sxs-lookup"><span data-stu-id="a6e9b-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="a6e9b-113">Enumerando Pins</span><span class="sxs-lookup"><span data-stu-id="a6e9b-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="a6e9b-114">Enumerando tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a6e9b-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="a6e9b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6e9b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6e9b-116">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a6e9b-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



