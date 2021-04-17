---
description: Resumo do encadeamento de filtro
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Resumo do encadeamento de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759530"
---
# <a name="summary-of-filter-threading"></a><span data-ttu-id="c38bc-103">Resumo do encadeamento de filtro</span><span class="sxs-lookup"><span data-stu-id="c38bc-103">Summary of Filter Threading</span></span>

<span data-ttu-id="c38bc-104">Os métodos a seguir são chamados no thread de streaming:</span><span class="sxs-lookup"><span data-stu-id="c38bc-104">The following methods are called on the streaming thread:</span></span>

-   [<span data-ttu-id="c38bc-105">**IMemInputPin:: receber**</span><span class="sxs-lookup"><span data-stu-id="c38bc-105">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="c38bc-106">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="c38bc-106">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="c38bc-107">**IPin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="c38bc-107">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="c38bc-108">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="c38bc-108">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [<span data-ttu-id="c38bc-109">**IMemAllocator::GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="c38bc-109">**IMemAllocator::GetBuffer**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

<span data-ttu-id="c38bc-110">Os métodos a seguir são chamados no thread do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c38bc-110">The following methods are called on the application thread:</span></span>

-   <span data-ttu-id="c38bc-111">Alterações de Estado: [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter:: execute**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span><span class="sxs-lookup"><span data-stu-id="c38bc-111">State changes: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span></span>
-   <span data-ttu-id="c38bc-112">Relógio de referência: [**IMediaFilter:: Getsyncname**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter:: setsyncname**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span><span class="sxs-lookup"><span data-stu-id="c38bc-112">Reference clock: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span></span>
-   <span data-ttu-id="c38bc-113">Operações de PIN: [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span><span class="sxs-lookup"><span data-stu-id="c38bc-113">Pin operations: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span></span>
-   <span data-ttu-id="c38bc-114">Funções de alocador: [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span><span class="sxs-lookup"><span data-stu-id="c38bc-114">Allocator functions: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span></span>
-   <span data-ttu-id="c38bc-115">Liberando: [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="c38bc-115">Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>

<span data-ttu-id="c38bc-116">Esta lista não é exaustiva.</span><span class="sxs-lookup"><span data-stu-id="c38bc-116">This list is not exhaustive.</span></span> <span data-ttu-id="c38bc-117">Ao implementar um filtro, você deve considerar quais métodos alteram o estado do filtro e quais métodos executam operações de streaming.</span><span class="sxs-lookup"><span data-stu-id="c38bc-117">When you implement a filter, you must consider which methods change the filter state, and which methods perform streaming operations.</span></span>

 

 



