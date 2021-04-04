---
description: Usando fontes de mídia com a sessão de mídia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Usando fontes de mídia com a sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930130"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="11996-103">Usando fontes de mídia com a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="11996-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="11996-104">Se você estiver usando a sessão de mídia para controlar a reprodução, o conjunto de métodos que você deve chamar em uma fonte de mídia será restrito.</span><span class="sxs-lookup"><span data-stu-id="11996-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="11996-105">Esta seção descreve como usar a origem de mídia em conjunto com a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="11996-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="11996-106">Aqui estão as etapas básicas que seu aplicativo executará:</span><span class="sxs-lookup"><span data-stu-id="11996-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="11996-107">Crie a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="11996-107">Create the media source.</span></span> <span data-ttu-id="11996-108">Para criar uma fonte de mídia, use o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="11996-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="11996-109">Para obter mais informações, consulte [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="11996-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="11996-110">O resolvedor de origem retorna um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte.</span><span class="sxs-lookup"><span data-stu-id="11996-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="11996-111">(Se você tiver escrito uma fonte de mídia personalizada, poderá fornecer um método de criação personalizado em vez disso.)</span><span class="sxs-lookup"><span data-stu-id="11996-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="11996-112">Configure a apresentação.</span><span class="sxs-lookup"><span data-stu-id="11996-112">Configure the presentation.</span></span> <span data-ttu-id="11996-113">Para configurar a apresentação da origem, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="11996-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="11996-114">Você pode modificar essa cópia, mas as alterações não se tornam ativas até que a reprodução seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="11996-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="11996-115">Não modifique o descritor de apresentação durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="11996-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="11996-116">Para obter mais informações, consulte [descritores de apresentação](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="11996-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="11996-117">Crie uma topologia que contenha a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="11996-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="11996-118">Para obter mais informações, consulte [topologias](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="11996-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="11996-119">Use a sessão de mídia para controlar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="11996-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="11996-120">A sessão de mídia chama métodos na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="11996-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="11996-121">O aplicativo não deve chamar nenhum método na origem da mídia no momento.</span><span class="sxs-lookup"><span data-stu-id="11996-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="11996-122">Antes de liberar a origem da mídia, chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a origem.</span><span class="sxs-lookup"><span data-stu-id="11996-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="11996-123">Se você estiver usando a origem do sequenciador, a origem do sequenciador manipulará o desligamento das fontes de segmento.</span><span class="sxs-lookup"><span data-stu-id="11996-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="11996-124">Para obter mais informações, consulte [origem do sequenciador](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="11996-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="11996-125">Se você usar a sessão de mídia, os únicos métodos que você deve chamar na origem da mídia são [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**getcaracterísticas**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="11996-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="11996-126">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="11996-126">In particular:</span></span>

-   <span data-ttu-id="11996-127">Não chame [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pausar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)ou [**parar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); Esses métodos devem ser chamados apenas pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="11996-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="11996-128">Não chame nenhum método [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .</span><span class="sxs-lookup"><span data-stu-id="11996-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="11996-129">Não recupere eventos diretamente da origem de mídia ou de qualquer um dos fluxos.</span><span class="sxs-lookup"><span data-stu-id="11996-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="11996-130">A sessão de mídia deve receber esses eventos para que o pipeline funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="11996-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="11996-131">A sessão de mídia encaminha todos os eventos que são necessários para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11996-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11996-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11996-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11996-133">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="11996-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



