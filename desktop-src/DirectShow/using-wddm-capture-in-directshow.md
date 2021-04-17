---
description: Usando a captura do WDDM no DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Usando a captura do WDDM no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770061"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="ba3a0-103">Usando a captura do WDDM no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba3a0-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="ba3a0-104">Este tópico aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="ba3a0-105">Algumas placas de vídeo têm a funcionalidade de captura de vídeo integrada.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="ba3a0-106">Nesses cartões, os quadros de vídeo capturados são colocados na memória de vídeo (VRAM).</span><span class="sxs-lookup"><span data-stu-id="ba3a0-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="ba3a0-107">Antes do Windows Vista, não havia nenhum mecanismo padrão para processar os quadros enquanto eles permaneceram em VRAM.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="ba3a0-108">Em vez disso, os dados tinham que ser copiados na memória do sistema, processados e, em seguida, copiados de volta para VRAM para exibição.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="ba3a0-109">No Windows Vista, o DirectShow agora dá suporte a um mecanismo para manter os quadros de vídeo em VRAM durante todo o pipeline de processamento, desde a captura até a exibição.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="ba3a0-110">O filtro KsProxy determina se o driver dá suporte à captura de superfície de VRAM consultando o driver para a \_ propriedade de superfície de captura preferencial KSPROPERTY \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="ba3a0-111">(Essa propriedade está documentada na documentação do kit de driver do Windows.) Se o driver oferecer suporte à captura de superfície de VRAM, o KsProxy alocará um tipo especial de exemplo de mídia que mantém um ponteiro para uma superfície do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="ba3a0-112">Em seguida, KsProxy determina se o filtro downstream dá suporte a DXVA (DirectX Video Acceleration) 2,0, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ba3a0-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="ba3a0-113">KsProxy consulta o pino de entrada downstream para a interface **IMFGetService** .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="ba3a0-114">Se o PIN expõe **IMFGetService**, KsProxy chama **IMFGetService:: GetService** para a interface **IDirect3DDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="ba3a0-115">O serviço identier é o \_ serviço de aceleração de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="ba3a0-116">Ambas as interfaces estão documentadas na documentação do SDK do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="ba3a0-117">Se o filtro downstream não der suporte a DXVA 2,0, o KsProxy alocará um buffer de memória do sistema adicional.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="ba3a0-118">Ele usa esse buffer para copiar os quadros de vídeo de VRAM para a memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="ba3a0-119">O método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) do exemplo de mídia retorna um ponteiro para esse buffer de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="ba3a0-120">No entanto, se o filtro downstream oferecer suporte a DXVA 2,0, o KsProxy não alocará um buffer de memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="ba3a0-121">Nesse caso, o método **Getapontarr** retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="ba3a0-122">Em vez disso, espera-se que o filtro downstream acesse a superfície do Direct3D de exemplo diretamente.</span><span class="sxs-lookup"><span data-stu-id="ba3a0-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="ba3a0-123">Há duas maneiras para o filtro downstream obter um ponteiro para a superfície, ambos equivalentes:</span><span class="sxs-lookup"><span data-stu-id="ba3a0-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="ba3a0-124">Consulte o exemplo para a interface **IMFGetService** e chame **GetService** para a interface **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="ba3a0-125">O identificador de serviço é o serviço de buffer do MR \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba3a0-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="ba3a0-126">Consulte o exemplo para a interface [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chame [**IMediaSample2Config:: getsurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="ba3a0-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba3a0-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba3a0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba3a0-128">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="ba3a0-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



