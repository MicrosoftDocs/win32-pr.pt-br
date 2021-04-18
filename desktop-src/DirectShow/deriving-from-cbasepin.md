---
description: Derivando de CBasePin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Derivando de CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778437"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="9d89f-103">Derivando de CBasePin</span><span class="sxs-lookup"><span data-stu-id="9d89f-103">Deriving from CBasePin</span></span>

<span data-ttu-id="9d89f-104">Para implementar um PIN usando [**CBasePin**](cbasepin.md), você deve derivar uma nova classe da classe base e substituir vários de seus métodos.</span><span class="sxs-lookup"><span data-stu-id="9d89f-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="9d89f-105">Você deve substituir os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="9d89f-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="9d89f-106">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="9d89f-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="9d89f-107">**CBasePin:: GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="9d89f-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="9d89f-108">Provavelmente, você precisará substituir estes métodos adicionais:</span><span class="sxs-lookup"><span data-stu-id="9d89f-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="9d89f-109">**CBasePin:: ativo**</span><span class="sxs-lookup"><span data-stu-id="9d89f-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="9d89f-110">**CBasePin::BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="9d89f-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="9d89f-111">**CBasePin::CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="9d89f-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="9d89f-112">**CBasePin::CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="9d89f-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="9d89f-113">**CBasePin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="9d89f-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="9d89f-114">**CBasePin:: inativo**</span><span class="sxs-lookup"><span data-stu-id="9d89f-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="9d89f-115">**CBasePin:: Notify**</span><span class="sxs-lookup"><span data-stu-id="9d89f-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="9d89f-116">**CBasePin:: Run**</span><span class="sxs-lookup"><span data-stu-id="9d89f-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="9d89f-117">Por fim, você deve implementar os métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="9d89f-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="9d89f-118">Alguns desses métodos são implementados em classes base que derivam de **CBasePin**, como [**CBaseInputPin**](cbaseinputpin.md) e [**CBaseOutputPin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="9d89f-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d89f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d89f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d89f-120">**CBasePin**</span><span class="sxs-lookup"><span data-stu-id="9d89f-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



