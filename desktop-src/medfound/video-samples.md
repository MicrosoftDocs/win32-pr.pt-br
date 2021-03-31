---
description: Exemplos de vídeo
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Exemplos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827792"
---
# <a name="video-samples"></a><span data-ttu-id="cc5f3-103">Exemplos de vídeo</span><span class="sxs-lookup"><span data-stu-id="cc5f3-103">Video Samples</span></span>

<span data-ttu-id="cc5f3-104">O objeto de exemplo de vídeo é uma implementação especializada da interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para uso com o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="cc5f3-105">Para criar uma instância desse objeto, chame a função [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) .</span><span class="sxs-lookup"><span data-stu-id="cc5f3-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="cc5f3-106">A função usa um ponteiro para uma superfície do Direct3D e retorna um ponteiro para a interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="cc5f3-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="cc5f3-107">Os seguintes tipos de objetos devem alocar amostras usando essa função:</span><span class="sxs-lookup"><span data-stu-id="cc5f3-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="cc5f3-108">Apresentadores de EVR personalizados.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-108">Custom EVR presenters.</span></span> <span data-ttu-id="cc5f3-109">Um apresentador aloca amostras de vídeo e as envia para o método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="cc5f3-110">Para obter mais informações, consulte [como escrever um apresentador EVR](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="cc5f3-111">Decodificadores de vídeo que dão suporte à aceleração de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="cc5f3-112">Para obter mais informações, consulte [dando suporte a DXVA 2,0 em Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="cc5f3-113">O objeto de exemplo de vídeo implementa as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="cc5f3-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="cc5f3-114">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="cc5f3-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="cc5f3-115">**IMFDesiredSample**</span><span class="sxs-lookup"><span data-stu-id="cc5f3-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="cc5f3-116">**IMFTrackedSample**</span><span class="sxs-lookup"><span data-stu-id="cc5f3-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="cc5f3-117">Se o parâmetro *pUnkSurface* de [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) for não **nulo**, o exemplo de vídeo resultante conterá um único buffer de mídia que encapsula a superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="cc5f3-118">Esse objeto de buffer tem funcionalidade limitada:</span><span class="sxs-lookup"><span data-stu-id="cc5f3-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="cc5f3-119">O método [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) do buffer retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="cc5f3-120">O buffer não implementa a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cc5f3-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="cc5f3-121">A única maneira de acessar a superfície do buffer é chamar [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), usando o serviço de buffer do Service Identifier Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5f3-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="cc5f3-122">Se o parâmetro *pUnkSurface* for **NULL**, o exemplo de vídeo será criado com zero buffers de mídia.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="cc5f3-123">Para adicionar um buffer ao exemplo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc5f3-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="cc5f3-124">Crie uma superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cc5f3-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="cc5f3-125">Crie um buffer de superfície chamando [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="cc5f3-126">Para obter mais informações, consulte [buffer de superfície DirectX](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="cc5f3-127">Adicione o buffer ao exemplo chamando [**IMFSample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span><span class="sxs-lookup"><span data-stu-id="cc5f3-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="cc5f3-128">Use essa abordagem se você precisar que a memória da superfície seja acessível por meio da interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cc5f3-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc5f3-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc5f3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc5f3-130">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="cc5f3-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="cc5f3-131">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="cc5f3-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
