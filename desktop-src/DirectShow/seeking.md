---
description: Atingir
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Atingir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104549941"
---
# <a name="seeking"></a><span data-ttu-id="19f20-103">Atingir</span><span class="sxs-lookup"><span data-stu-id="19f20-103">Seeking</span></span>

<span data-ttu-id="19f20-104">Os filtros dão suporte à busca por meio da interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="19f20-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="19f20-105">O aplicativo consulta o Gerenciador de gráfico de filtro para **IMediaSeeking** e o usa para emitir comandos de busca.</span><span class="sxs-lookup"><span data-stu-id="19f20-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="19f20-106">O Gerenciador de gráfico de filtro distribui cada comando de busca para todos os filtros de processador no grafo.</span><span class="sxs-lookup"><span data-stu-id="19f20-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="19f20-107">Cada renderizador passa o comando upstream, por meio dos Pins de saída dos filtros upstream, até alcançar um filtro que possa executar a busca.</span><span class="sxs-lookup"><span data-stu-id="19f20-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="19f20-108">Normalmente, um filtro de origem ou um filtro de analisador, como o [divisor AVI](avi-splitter-filter.md), executa a operação de busca.</span><span class="sxs-lookup"><span data-stu-id="19f20-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="19f20-109">Quando um filtro executa uma operação de busca, ele libera todos os dados pendentes.</span><span class="sxs-lookup"><span data-stu-id="19f20-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="19f20-110">O resultado é minimizar a latência de comandos de busca, pois os dados existentes são liberados do grafo.</span><span class="sxs-lookup"><span data-stu-id="19f20-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="19f20-111">Após um comando de busca, o tempo de fluxo é redefinido como zero.</span><span class="sxs-lookup"><span data-stu-id="19f20-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="19f20-112">O diagrama a seguir ilustra a sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="19f20-112">The following diagram illustrates the sequence of events.</span></span>

![sequência de eventos](images/seeking.png)

<span data-ttu-id="19f20-114">Se um filtro do analisador tiver mais de um pino de saída, ele normalmente designará um deles para aceitar comandos de busca.</span><span class="sxs-lookup"><span data-stu-id="19f20-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="19f20-115">Os outros Pins rejeitam ou ignoram os comandos de busca recebidos.</span><span class="sxs-lookup"><span data-stu-id="19f20-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="19f20-116">Dessa forma, o analisador mantém todos os seus fluxos sincronizados.</span><span class="sxs-lookup"><span data-stu-id="19f20-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="19f20-117">No entanto, todos os Pins de saída devem implementar [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) e [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) para retornar os recursos de busca do filtro.</span><span class="sxs-lookup"><span data-stu-id="19f20-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="19f20-118">Isso garante que o Gerenciador de gráfico de filtro retorne o valor correto para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19f20-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="19f20-119">A interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) foi preterida para filtros.</span><span class="sxs-lookup"><span data-stu-id="19f20-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="19f20-120">Os clientes de automação ainda precisam usar essa interface no Gerenciador de gráficos de filtro, porque **IMediaSeeking** não é compatível com a automação, mas o Gerenciador de grafo de filtro converte todas as chamadas **IMediaPosition** em chamadas **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="19f20-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19f20-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19f20-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f20-122">Liberação</span><span class="sxs-lookup"><span data-stu-id="19f20-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="19f20-123">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="19f20-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



