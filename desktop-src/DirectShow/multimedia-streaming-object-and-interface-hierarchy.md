---
description: Hierarquia de interface e objeto de streaming de multimídia
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Hierarquia de interface e objeto de streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837685"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="834d4-103">Hierarquia de interface e objeto de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="834d4-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="834d4-104">Essas APIs são preteridas.</span><span class="sxs-lookup"><span data-stu-id="834d4-104">These APIs are deprecated.</span></span> <span data-ttu-id="834d4-105">Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="834d4-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="834d4-106">O diagrama a seguir mostra a hierarquia de objetos usada no streaming de multimídia.</span><span class="sxs-lookup"><span data-stu-id="834d4-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![hierarquia de objetos multimediastreaming](images/mmstream02.png)

<span data-ttu-id="834d4-108">A arquitetura de streaming de multimídia define três tipos gerais de objeto:</span><span class="sxs-lookup"><span data-stu-id="834d4-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="834d4-109">O objeto **AMMultimediaStream** expõe a interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) .</span><span class="sxs-lookup"><span data-stu-id="834d4-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="834d4-110">Internamente, esse objeto encapsula o grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="834d4-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="834d4-111">Os objetos de *fluxo de mídia* expõem a interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e são específicos de dados.</span><span class="sxs-lookup"><span data-stu-id="834d4-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="834d4-112">O objeto AMMultimediaStream contém um ou mais fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="834d4-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="834d4-113">Os objetos de *exemplo de fluxo* contêm os dados para um fluxo específico.</span><span class="sxs-lookup"><span data-stu-id="834d4-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="834d4-114">Há suporte para os seguintes objetos de fluxo de mídia:</span><span class="sxs-lookup"><span data-stu-id="834d4-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="834d4-115">Fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="834d4-115">Audio stream.</span></span> <span data-ttu-id="834d4-116">Expõe a interface [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .</span><span class="sxs-lookup"><span data-stu-id="834d4-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="834d4-117">Fluxo do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="834d4-117">DirectDraw stream.</span></span> <span data-ttu-id="834d4-118">Representa um fluxo de vídeo que é processado para uma superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="834d4-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="834d4-119">Expõe a interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .</span><span class="sxs-lookup"><span data-stu-id="834d4-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="834d4-120">Fluxo do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="834d4-120">Media type stream.</span></span> <span data-ttu-id="834d4-121">Representa dados arbitrários.</span><span class="sxs-lookup"><span data-stu-id="834d4-121">Represents arbitrary data.</span></span> <span data-ttu-id="834d4-122">Expõe a interface [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .</span><span class="sxs-lookup"><span data-stu-id="834d4-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="834d4-123">Cada objeto de fluxo de mídia cria seu próprio tipo de objeto de exemplo de fluxo:</span><span class="sxs-lookup"><span data-stu-id="834d4-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="834d4-124">Fluxos de áudio criam amostras de áudio, que expõem a interface [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="834d4-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="834d4-125">Os fluxos do DirectDraw criam exemplos do DirectDraw, que expõem a interface [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="834d4-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="834d4-126">Os fluxos de tipo de mídia criam amostras de tipo de mídia, que expõem a interface [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .</span><span class="sxs-lookup"><span data-stu-id="834d4-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="834d4-127">O diagrama a seguir mostra a hierarquia de interface para as interfaces listadas anteriormente:</span><span class="sxs-lookup"><span data-stu-id="834d4-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![hierarquia de interface multimediastreaming](images/mmstream01.png)

 

 



