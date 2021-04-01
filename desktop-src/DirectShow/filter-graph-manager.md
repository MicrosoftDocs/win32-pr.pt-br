---
description: Gerenciador de gráfico de filtro
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gerenciador de gráfico de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825517"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="3bbfb-103">Gerenciador de gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="3bbfb-103">Filter Graph Manager</span></span>

<span data-ttu-id="3bbfb-104">O Gerenciador de gráficos de filtro cria e controla os gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="3bbfb-105">Esse objeto é o componente central no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="3bbfb-106">Os aplicativos o usam para criar e controlar gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="3bbfb-107">O Gerenciador de gráficos de filtro também trata da sincronização, da notificação de eventos e de outros aspectos do controle do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="3bbfb-108">Crie esse objeto chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="3bbfb-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="3bbfb-109">CLSID</span></span>

<span data-ttu-id="3bbfb-110">Há dois CLSIDs para criar o Gerenciador de gráficos de filtro:</span><span class="sxs-lookup"><span data-stu-id="3bbfb-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="3bbfb-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="3bbfb-111">CLSID</span></span>                      | <span data-ttu-id="3bbfb-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bbfb-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="3bbfb-113">\_FILTERGRAPH CLSID</span><span class="sxs-lookup"><span data-stu-id="3bbfb-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="3bbfb-114">Cria o Gerenciador de gráfico de filtro em um thread de trabalho compartilhado.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="3bbfb-115">\_FILTERGRAPHNOTHREAD CLSID</span><span class="sxs-lookup"><span data-stu-id="3bbfb-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="3bbfb-116">Cria o Gerenciador de gráfico de filtro no thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="3bbfb-117">Em geral, os aplicativos devem usar CLSID \_ FilterGraph.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="3bbfb-118">Ambos os CLSIDs criam o mesmo objeto, mas usam modelos de Threading diferentes:</span><span class="sxs-lookup"><span data-stu-id="3bbfb-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="3bbfb-119">CLSID \_ FilterGraph cria o Gerenciador de gráfico de filtro em um thread de trabalho, que é compartilhado por todas as \_ instâncias de FILTERGRAPH do CLSID dentro do mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="3bbfb-120">O thread despacha mensagens enviadas por filtros e controla o tempo de vida de qualquer Windows criado por filtros.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="3bbfb-121">CLSID \_ FilterGraphNoThread cria o Gerenciador de gráfico de filtro no thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="3bbfb-122">Se você usar esse CLSID, o thread que chama **CoCreateInstance** deverá ter um loop de mensagem que expedir mensagens; caso contrário, podem ocorrer deadlocks.</span><span class="sxs-lookup"><span data-stu-id="3bbfb-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="3bbfb-123">Além disso, antes de o thread do aplicativo sair, ele deve liberar o Gerenciador do grafo de filtro e todos os objetos do grafo (como filtros, Pins, relógios de referência e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="3bbfb-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="3bbfb-124">Interfaces</span><span class="sxs-lookup"><span data-stu-id="3bbfb-124">Interfaces</span></span>

<span data-ttu-id="3bbfb-125">O Gerenciador de gráficos de filtro expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3bbfb-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="3bbfb-126">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="3bbfb-127">**IAMStats**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="3bbfb-128">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="3bbfb-129">**IBasicVideo**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="3bbfb-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="3bbfb-131">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="3bbfb-132">**IFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="3bbfb-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="3bbfb-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="3bbfb-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="3bbfb-136">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="3bbfb-137">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="3bbfb-138">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="3bbfb-139">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="3bbfb-140">**IMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="3bbfb-141">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="3bbfb-142">**IMediaEventSink**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="3bbfb-143">**IMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="3bbfb-144">**IMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="3bbfb-145">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="3bbfb-146">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="3bbfb-147">**IRegisterServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="3bbfb-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="3bbfb-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="3bbfb-150">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="3bbfb-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="3bbfb-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="3bbfb-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bbfb-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bbfb-153">Objetos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3bbfb-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



