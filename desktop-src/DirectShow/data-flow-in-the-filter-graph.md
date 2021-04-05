---
description: Fluxo de dados no grafo de filtro
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Fluxo de dados no grafo de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826014"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="d2d6d-103">Fluxo de dados no grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="d2d6d-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="d2d6d-104">Esta seção descreve como os dados de mídia são movidos pelo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="d2d6d-105">Normalmente, você não precisa saber esses detalhes para escrever um aplicativo do DirectShow, embora em algumas situações possa achar útil.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="d2d6d-106">Se estiver escrevendo um filtro do DirectShow, você precisará entender esse material.</span><span class="sxs-lookup"><span data-stu-id="d2d6d-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="d2d6d-107">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d2d6d-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d2d6d-108">Visão geral do fluxo de dados no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d2d6d-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="d2d6d-109">Transportes</span><span class="sxs-lookup"><span data-stu-id="d2d6d-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="d2d6d-110">Exemplos e alocadores</span><span class="sxs-lookup"><span data-stu-id="d2d6d-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="d2d6d-111">Estados de filtro</span><span class="sxs-lookup"><span data-stu-id="d2d6d-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="d2d6d-112">Modelo de Pull</span><span class="sxs-lookup"><span data-stu-id="d2d6d-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="d2d6d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2d6d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2d6d-114">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="d2d6d-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



