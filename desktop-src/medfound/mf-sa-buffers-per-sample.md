---
description: Especifica quantos buffers o alocador de vídeo do exemplo cria para cada amostra de vídeo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Atributo MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647568"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="8d438-103">\_Buffers de SA de MF \_ \_ por \_ atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8d438-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="8d438-104">Especifica quantos buffers o alocador de vídeo do exemplo cria para cada amostra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8d438-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="8d438-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8d438-105">Data type</span></span>

<span data-ttu-id="8d438-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8d438-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8d438-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d438-107">Remarks</span></span>

<span data-ttu-id="8d438-108">Se você usar a interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para alocar amostras de vídeo, poderá usar esse atributo para criar amostras de vídeo que contenham vários buffers.</span><span class="sxs-lookup"><span data-stu-id="8d438-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="8d438-109">Por exemplo, se o valor do atributo for 2, o alocador criará dois buffers de vídeo para cada amostra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8d438-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="8d438-110">Defina o atributo no parâmetro *pAttributes* do método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="8d438-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="8d438-111">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="8d438-111">The default value is 1.</span></span> <span data-ttu-id="8d438-112">Se o atributo não estiver definido, o alocador criará amostras de vídeo que contenham um único buffer por amostra.</span><span class="sxs-lookup"><span data-stu-id="8d438-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="8d438-113">Esse atributo destina-se principalmente a transformações de Media Foundation (MFTs) que dão suporte à saída 3D estéreo, na seguinte situação:</span><span class="sxs-lookup"><span data-stu-id="8d438-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="8d438-114">A MFT dá suporte à Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="8d438-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="8d438-115">O MFT aloca seus próprios exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="8d438-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="8d438-116">O MFT usa a interface [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para alocar os exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="8d438-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="8d438-117">O formato de vídeo 3D usa um buffer separado para cada exibição.</span><span class="sxs-lookup"><span data-stu-id="8d438-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="8d438-118">Se todos esses critérios forem verdadeiros, o MFT deverá definir o valor do atributo como 2 (um buffer por exibição).</span><span class="sxs-lookup"><span data-stu-id="8d438-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d438-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d438-119">Requirements</span></span>



| <span data-ttu-id="8d438-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d438-120">Requirement</span></span> | <span data-ttu-id="8d438-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8d438-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d438-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d438-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d438-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8d438-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="8d438-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d438-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d438-125">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8d438-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8d438-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d438-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d438-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d438-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d438-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d438-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d438-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d438-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




