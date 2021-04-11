---
description: Técnicas de Graph-Building geral
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Técnicas de Graph-Building geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163702"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="f5097-103">Técnicas de Graph-Building geral</span><span class="sxs-lookup"><span data-stu-id="f5097-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="f5097-104">Cada aplicativo do DirectShow começa com a criação de um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5097-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="f5097-105">Ao ler os tópicos de visão geral na documentação do DirectShow, você descobrirá que a maioria começa descrevendo o tipo de grafo de filtro necessário.</span><span class="sxs-lookup"><span data-stu-id="f5097-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="f5097-106">Em alguns casos, há um método ou um objeto auxiliar especificamente projetado para a criação desse tipo de grafo.</span><span class="sxs-lookup"><span data-stu-id="f5097-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="f5097-107">Por exemplo, o objeto do [Construtor de gráficos de DVD](dvd-graph-builder.md) cria grafos de reprodução de DVD.</span><span class="sxs-lookup"><span data-stu-id="f5097-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="f5097-108">Em outros casos, o aplicativo deve construir o grafo adicionando filtros e conectando-os.</span><span class="sxs-lookup"><span data-stu-id="f5097-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="f5097-109">Esta seção apresenta algumas funções auxiliares que implementam operações básicas de criação de gráficos.</span><span class="sxs-lookup"><span data-stu-id="f5097-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="f5097-110">Eles podem ser usados por qualquer aplicativo do DirectShow que precise criar ou modificar um gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="f5097-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="f5097-111">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f5097-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="f5097-112">Adicionar um filtro por CLSID</span><span class="sxs-lookup"><span data-stu-id="f5097-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="f5097-113">Localizar um PIN não conectado em um filtro</span><span class="sxs-lookup"><span data-stu-id="f5097-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="f5097-114">Conectar dois filtros</span><span class="sxs-lookup"><span data-stu-id="f5097-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="f5097-115">Localizar uma interface em um filtro ou PIN</span><span class="sxs-lookup"><span data-stu-id="f5097-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="f5097-116">Localizar o par de um filtro</span><span class="sxs-lookup"><span data-stu-id="f5097-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="f5097-117">Remover todos os filtros no grafo</span><span class="sxs-lookup"><span data-stu-id="f5097-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="f5097-118">Criando gráficos com o construtor de grafo de captura</span><span class="sxs-lookup"><span data-stu-id="f5097-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="f5097-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5097-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5097-120">Tarefas básicas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f5097-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="f5097-121">Enumerando dispositivos e filtros</span><span class="sxs-lookup"><span data-stu-id="f5097-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="f5097-122">Enumerando objetos em um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="f5097-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="f5097-123">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="f5097-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



