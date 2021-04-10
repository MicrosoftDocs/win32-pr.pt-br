---
description: Benefícios do DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Benefícios do DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163841"
---
# <a name="benefits-of-dmos"></a><span data-ttu-id="7b53f-103">Benefícios do DMOs</span><span class="sxs-lookup"><span data-stu-id="7b53f-103">Benefits of DMOs</span></span>

<span data-ttu-id="7b53f-104">O DMOs oferece as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="7b53f-104">DMOs offer the following advantages:</span></span>

-   <span data-ttu-id="7b53f-105">Eles são geralmente menores e mais simples que os filtros do DirectShow, pois oferecem suporte a menos funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="7b53f-105">They are generally smaller and simpler than DirectShow filters, because they support less functionality.</span></span>
-   <span data-ttu-id="7b53f-106">Eles são mais flexíveis do que os filtros do DirectShow porque não exigem um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7b53f-106">They are more flexible than DirectShow filters because they do not require a filter graph.</span></span> <span data-ttu-id="7b53f-107">Você pode usá-los com o DirectShow quando precisar dos serviços que o DirectShow fornece, como sincronização, conexão inteligente, manipulação automática de fluxo de dados e gerenciamento de threads.</span><span class="sxs-lookup"><span data-stu-id="7b53f-107">You can use them with DirectShow when you need the services that DirectShow provides, such as synchronization, intelligent connection, automatic handling of data flow, and thread management.</span></span> <span data-ttu-id="7b53f-108">Os clientes que não precisam desses serviços podem acessar o DMOs diretamente.</span><span class="sxs-lookup"><span data-stu-id="7b53f-108">Clients that do not need these services can access DMOs directly.</span></span>
-   <span data-ttu-id="7b53f-109">O DMOs sempre executa o processamento de dados síncrono, o que elimina muitos dos problemas de Threading que você deve considerar se escrever um filtro.</span><span class="sxs-lookup"><span data-stu-id="7b53f-109">DMOs always perform synchronous data processing, which eliminates many of the threading issues that you must consider if you write a filter.</span></span>
-   <span data-ttu-id="7b53f-110">Ao contrário dos codecs ACM e VCM tradicionais, os DMOs são baseados na Component Object Model (COM), para que possam ser estendidos por meio de **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7b53f-110">Unlike traditional ACM and VCM codecs, DMOs are based on the Component Object Model (COM), so they can be extended through **QueryInterface**.</span></span>
-   <span data-ttu-id="7b53f-111">O DMOs dá suporte a um modelo de streaming mais generalizado que os codecs ACM ou VCM.</span><span class="sxs-lookup"><span data-stu-id="7b53f-111">DMOs support a more generalized streaming model than ACM or VCM codecs.</span></span> <span data-ttu-id="7b53f-112">Assim como os filtros do DirectShow, o DMOs pode dar suporte a várias entradas e várias saídas.</span><span class="sxs-lookup"><span data-stu-id="7b53f-112">Like DirectShow filters, DMOs can support multiple inputs and multiple outputs.</span></span>

<span data-ttu-id="7b53f-113">Por esses motivos, DMOs agora são recomendados como a solução para escrever codificadores, decodificadores e efeitos de áudio.</span><span class="sxs-lookup"><span data-stu-id="7b53f-113">For these reasons, DMOs are now recommended as the solution for writing encoders, decoders, and audio effects.</span></span> <span data-ttu-id="7b53f-114">Muitos outros cenários também são possíveis, dependendo das necessidades do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b53f-114">Many other scenarios are possible as well, depending on the needs of the application.</span></span>

<span data-ttu-id="7b53f-115">Como o DMOs difere dos filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7b53f-115">How DMOs Differ from DirectShow Filters</span></span>

<span data-ttu-id="7b53f-116">Os filtros do DirectShow não podem funcionar fora de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7b53f-116">DirectShow filters cannot function outside of a DirectShow filter graph.</span></span> <span data-ttu-id="7b53f-117">No DirectShow, o Gerenciador de gráfico de filtro é corrigido entre o aplicativo e os filtros.</span><span class="sxs-lookup"><span data-stu-id="7b53f-117">In DirectShow, the Filter Graph Manager mediates between the application and the filters.</span></span> <span data-ttu-id="7b53f-118">Os filtros do DirectShow fazem a maior parte do trabalho necessário para transmitir dados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="7b53f-118">DirectShow filters do most of the work required to stream data, including:</span></span>

-   <span data-ttu-id="7b53f-119">Alocando buffers.</span><span class="sxs-lookup"><span data-stu-id="7b53f-119">Allocating buffers.</span></span>
-   <span data-ttu-id="7b53f-120">Negociando tipos de mídia e conexões com outros filtros.</span><span class="sxs-lookup"><span data-stu-id="7b53f-120">Negotiating media types and connections to other filters.</span></span>
-   <span data-ttu-id="7b53f-121">Enviar dados por push pelo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="7b53f-121">Pushing data through the filter graph.</span></span>
-   <span data-ttu-id="7b53f-122">Enviando eventos para o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="7b53f-122">Sending events to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="7b53f-123">Sincronizando vários threads.</span><span class="sxs-lookup"><span data-stu-id="7b53f-123">Synchronizing multiple threads.</span></span>

<span data-ttu-id="7b53f-124">Por outro lado, um DMO não faz nenhuma dessas coisas.</span><span class="sxs-lookup"><span data-stu-id="7b53f-124">In contrast, a DMO does none of these things.</span></span> <span data-ttu-id="7b53f-125">Em vez disso, esses tipos de tarefas são responsabilidade do cliente usando o DMO.</span><span class="sxs-lookup"><span data-stu-id="7b53f-125">Instead, these kinds of tasks are the responsibility of the client using the DMO.</span></span> <span data-ttu-id="7b53f-126">O cliente aloca buffers, preenche-os com dados e os entrega para o DMO.</span><span class="sxs-lookup"><span data-stu-id="7b53f-126">The client allocates buffers, fills them with data, and delivers them to the DMO.</span></span> <span data-ttu-id="7b53f-127">O DMO processa os dados e o cliente recupera os buffers de saída resultantes.</span><span class="sxs-lookup"><span data-stu-id="7b53f-127">The DMO processes the data, and the client retrieves the resulting output buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b53f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b53f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b53f-129">Sobre o DMOs</span><span class="sxs-lookup"><span data-stu-id="7b53f-129">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



