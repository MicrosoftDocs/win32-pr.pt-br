---
description: Gerenciamento de Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gerenciamento de Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758832"
---
# <a name="quality-control-management"></a><span data-ttu-id="61a9f-103">Gerenciamento de Quality-Control</span><span class="sxs-lookup"><span data-stu-id="61a9f-103">Quality-Control Management</span></span>

<span data-ttu-id="61a9f-104">O controle de qualidade é um mecanismo para ajustar a taxa de fluxo de dados por meio do grafo de filtro em resposta ao desempenho em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="61a9f-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="61a9f-105">Se um filtro de processador estiver recebendo muitos dados ou poucos dados, ele poderá enviar uma *mensagem de qualidade*.</span><span class="sxs-lookup"><span data-stu-id="61a9f-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="61a9f-106">A mensagem de qualidade solicita um ajuste na taxa de dados.</span><span class="sxs-lookup"><span data-stu-id="61a9f-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="61a9f-107">Por padrão, as mensagens de qualidade viajam para upstream a partir do renderizador até chegarem a um filtro que pode responder (se houver).</span><span class="sxs-lookup"><span data-stu-id="61a9f-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="61a9f-108">Um aplicativo também pode implementar um Gerenciador de qualidade personalizado.</span><span class="sxs-lookup"><span data-stu-id="61a9f-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="61a9f-109">Nesse caso, o renderizador passa mensagens de qualidade diretamente para o Gerenciador de qualidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61a9f-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="61a9f-110">Este artigo contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="61a9f-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="61a9f-111">Mensagens de qualidade</span><span class="sxs-lookup"><span data-stu-id="61a9f-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="61a9f-112">Controle de qualidade padrão</span><span class="sxs-lookup"><span data-stu-id="61a9f-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="61a9f-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61a9f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a9f-114">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="61a9f-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="61a9f-115">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="61a9f-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



