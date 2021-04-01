---
description: Define a abertura geométrica para um tipo de mídia de vídeo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Atributo MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921267"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="1afb6-103">\_Atributo de \_ abertura geométrica do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="1afb6-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="1afb6-104">Define a abertura geométrica para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1afb6-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1afb6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1afb6-105">Data type</span></span>

<span data-ttu-id="1afb6-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="1afb6-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1afb6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1afb6-107">Remarks</span></span>

<span data-ttu-id="1afb6-108">O valor desse atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="1afb6-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="1afb6-109">A taxa de proporção da imagem é calculada em relação à abertura geométrica, usando a fórmula a seguir: taxa de proporção da imagem = (largura da abertura geométrica/altura da abertura geométrica) × taxa de proporção do pixel.</span><span class="sxs-lookup"><span data-stu-id="1afb6-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="1afb6-110">Se esse atributo não for definido, a abertura geométrica será considerada como o quadro de vídeo inteiro.</span><span class="sxs-lookup"><span data-stu-id="1afb6-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="1afb6-111">Você deve definir esse atributo somente quando o tipo de mídia descrever um padrão de vídeo com uma área ativa definida.</span><span class="sxs-lookup"><span data-stu-id="1afb6-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="1afb6-112">Por exemplo, na televisão NTSC, o quadro de vídeo é 720 × 480 com uma área ativa de 704 × 480 e uma taxa de proporção de 10:11 pixels.</span><span class="sxs-lookup"><span data-stu-id="1afb6-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="1afb6-113">A imagem resultante tem uma taxa de proporção de (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="1afb6-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="1afb6-114">O apresentador padrão para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) mostra a abertura geométrica do vídeo, se especificado.</span><span class="sxs-lookup"><span data-stu-id="1afb6-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="1afb6-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1afb6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="1afb6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1afb6-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="1afb6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1afb6-117">Requirements</span></span>



| <span data-ttu-id="1afb6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1afb6-118">Requirement</span></span> | <span data-ttu-id="1afb6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1afb6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1afb6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1afb6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1afb6-121">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="1afb6-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1afb6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1afb6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1afb6-123">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1afb6-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1afb6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1afb6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1afb6-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1afb6-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1afb6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1afb6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1afb6-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1afb6-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1afb6-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1afb6-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1afb6-129">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="1afb6-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="1afb6-130">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="1afb6-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="1afb6-131">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="1afb6-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1afb6-132">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="1afb6-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1afb6-133">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1afb6-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1afb6-134">**\_abertura de \_ \_ exibição mínima \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="1afb6-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="1afb6-135">**\_abertura de \_ digitalização de Pan MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="1afb6-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




