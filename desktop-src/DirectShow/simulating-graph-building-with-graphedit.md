---
description: Simulando a criação de gráficos com o GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulando a criação de gráficos com o GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456686"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="36c30-103">Simulando a criação de gráficos com o GraphEdit</span><span class="sxs-lookup"><span data-stu-id="36c30-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="36c30-104">O DirectShow fornece um utilitário de depuração chamado GraphEdit, que pode ser usado para criar e testar grafos de filtro.</span><span class="sxs-lookup"><span data-stu-id="36c30-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="36c30-105">GraphEdit é uma ferramenta Visual para criar gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="36c30-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="36c30-106">Com o GraphEdit, você pode experimentar um grafo de filtro antes de escrever qualquer código de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36c30-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="36c30-107">Você também pode carregar um grafo de filtro que seu aplicativo cria, para verificar se seu aplicativo está criando o grafo correto.</span><span class="sxs-lookup"><span data-stu-id="36c30-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="36c30-108">Se você desenvolver um filtro personalizado, o GraphEdit fornecerá uma maneira rápida de testá-lo: basta carregar um grafo com seu filtro personalizado e tentar executar o grafo.</span><span class="sxs-lookup"><span data-stu-id="36c30-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="36c30-109">Se você for novo no DirectShow, o GraphEdit é uma boa maneira de se familiarizar com grafos de filtro e com a arquitetura do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="36c30-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="36c30-110">A ilustração a seguir mostra como GraphEdit representa um gráfico de filtro simples.</span><span class="sxs-lookup"><span data-stu-id="36c30-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![Grafo de filtro simples em GraphEdit](images/gedit09.png)

<span data-ttu-id="36c30-112">Cada filtro é representado como um retângulo.</span><span class="sxs-lookup"><span data-stu-id="36c30-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="36c30-113">Quadrados menores ao longo das bordas dos filtros representam Pins.</span><span class="sxs-lookup"><span data-stu-id="36c30-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="36c30-114">Os Pins de entrada estão no lado esquerdo do filtro, e os Pins de saída estão no lado direito.</span><span class="sxs-lookup"><span data-stu-id="36c30-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="36c30-115">As setas representam as conexões entre os Pins.</span><span class="sxs-lookup"><span data-stu-id="36c30-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="36c30-116">Com o GraphEdit, você pode:</span><span class="sxs-lookup"><span data-stu-id="36c30-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="36c30-117">Criar e modificar gráficos de filtro usando uma interface visual, arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="36c30-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="36c30-118">Simular chamadas programáticas para criar um grafo.</span><span class="sxs-lookup"><span data-stu-id="36c30-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="36c30-119">Executar, pausar, parar e buscar um grafo.</span><span class="sxs-lookup"><span data-stu-id="36c30-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="36c30-120">Veja quais filtros estão registrados em seu computador e exiba informações de registro para cada filtro.</span><span class="sxs-lookup"><span data-stu-id="36c30-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="36c30-121">Exibir páginas de propriedades de filtro.</span><span class="sxs-lookup"><span data-stu-id="36c30-121">View filter property pages.</span></span>
-   <span data-ttu-id="36c30-122">Exiba os tipos de mídia de conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="36c30-122">View the media types of pin connections.</span></span>

<span data-ttu-id="36c30-123">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="36c30-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="36c30-124">Usando GraphEdit</span><span class="sxs-lookup"><span data-stu-id="36c30-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="36c30-125">Carregando um grafo a partir de um processo externo</span><span class="sxs-lookup"><span data-stu-id="36c30-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="36c30-126">Salvando um grafo de filtro em um arquivo GraphEdit</span><span class="sxs-lookup"><span data-stu-id="36c30-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="36c30-127">Carregando um arquivo GraphEdit programaticamente</span><span class="sxs-lookup"><span data-stu-id="36c30-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="36c30-128">Formato de arquivo GraphEdit</span><span class="sxs-lookup"><span data-stu-id="36c30-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="36c30-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36c30-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c30-130">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="36c30-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



