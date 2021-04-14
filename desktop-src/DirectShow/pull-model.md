---
description: Modelo de pull
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modelo de pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500373"
---
# <a name="pull-model"></a><span data-ttu-id="b5e12-103">Modelo de pull</span><span class="sxs-lookup"><span data-stu-id="b5e12-103">Pull Model</span></span>

<span data-ttu-id="b5e12-104">Na interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , o filtro upstream determina quais dados enviar e envia os dados para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="b5e12-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="b5e12-105">Para alguns filtros, um modelo de *pull* é mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="b5e12-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="b5e12-106">Aqui, o filtro downstream solicita dados do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="b5e12-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="b5e12-107">Os exemplos ainda viajam downstream, do pino de saída para o pino de entrada, mas o filtro downstream inicia o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5e12-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="b5e12-108">Esse tipo de conexão usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="b5e12-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="b5e12-109">O uso típico para o modelo de pull está na reprodução de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b5e12-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="b5e12-110">Por exemplo, em um grafo de reprodução AVI, o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) executa operações genéricas de leitura de arquivo e entrega os dados como um fluxo de bytes, sem informações de formato.</span><span class="sxs-lookup"><span data-stu-id="b5e12-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="b5e12-111">O filtro [AVI Splitter](avi-splitter-filter.md) lê os cabeçalhos AVI e analisa o fluxo em exemplos de vídeo e áudio.</span><span class="sxs-lookup"><span data-stu-id="b5e12-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="b5e12-112">O divisor AVI pode determinar quais dados precisam ser melhores do que o filtro de origem de arquivo assíncrono e, portanto, usa **IAsyncReader** em vez de **IMemInputPin**.</span><span class="sxs-lookup"><span data-stu-id="b5e12-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="b5e12-113">Para solicitar dados do pino de saída, o pino de entrada chama um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="b5e12-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="b5e12-114">**IAsyncReader:: solicitação**</span><span class="sxs-lookup"><span data-stu-id="b5e12-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="b5e12-115">**IAsyncReader::SyncRead**</span><span class="sxs-lookup"><span data-stu-id="b5e12-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="b5e12-116">[**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="b5e12-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="b5e12-117">O primeiro método é assíncrono, para dar suporte a várias leituras sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="b5e12-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="b5e12-118">Os outros são síncronos.</span><span class="sxs-lookup"><span data-stu-id="b5e12-118">The others are synchronous.</span></span>

<span data-ttu-id="b5e12-119">Teoricamente, qualquer filtro pode dar suporte a **IAsyncReader**, mas, na prática, ele foi projetado para filtros de origem que se conectam a filtros do analisador.</span><span class="sxs-lookup"><span data-stu-id="b5e12-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="b5e12-120">O analisador age muito como um filtro de origem no modelo de push.</span><span class="sxs-lookup"><span data-stu-id="b5e12-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="b5e12-121">Quando ele pausa, ele cria um thread de streaming que efetua pull de dados da conexão **IAsyncReader** e o envia por push para o downstream.</span><span class="sxs-lookup"><span data-stu-id="b5e12-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="b5e12-122">Os Pins de saída usam **IMemInputPin** e o restante do grafo usa o modelo Push padrão.</span><span class="sxs-lookup"><span data-stu-id="b5e12-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5e12-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5e12-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e12-124">Fluxo de dados no grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="b5e12-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



