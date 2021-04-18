---
description: Define a abertura de exibição, que é a região de um quadro de vídeo que contém dados de imagem válidos.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Atributo MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768357"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="85ca1-103">\_Atributo de \_ \_ abertura de exibição mínima \_ de MF MT</span><span class="sxs-lookup"><span data-stu-id="85ca1-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="85ca1-104">Define a abertura de exibição, que é a região de um quadro de vídeo que contém dados de imagem válidos.</span><span class="sxs-lookup"><span data-stu-id="85ca1-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="85ca1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="85ca1-105">Data type</span></span>

<span data-ttu-id="85ca1-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="85ca1-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="85ca1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="85ca1-107">Remarks</span></span>

<span data-ttu-id="85ca1-108">O valor do atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="85ca1-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="85ca1-109">A abertura de exibição mínima é a região que contém a parte válida do sinal.</span><span class="sxs-lookup"><span data-stu-id="85ca1-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="85ca1-110">Os pixels fora da abertura contêm dados inválidos e não devem ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="85ca1-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="85ca1-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="85ca1-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ca1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85ca1-112">Requirements</span></span>



| <span data-ttu-id="85ca1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ca1-113">Requirement</span></span> | <span data-ttu-id="85ca1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="85ca1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85ca1-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85ca1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="85ca1-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="85ca1-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="85ca1-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85ca1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="85ca1-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="85ca1-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="85ca1-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85ca1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ca1-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ca1-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ca1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="85ca1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ca1-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85ca1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85ca1-123">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="85ca1-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="85ca1-124">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="85ca1-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="85ca1-125">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="85ca1-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="85ca1-126">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="85ca1-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="85ca1-127">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="85ca1-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="85ca1-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="85ca1-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="85ca1-129">**\_ \_ abertura geométrica do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="85ca1-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="85ca1-130">**\_abertura de \_ digitalização de Pan MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="85ca1-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




