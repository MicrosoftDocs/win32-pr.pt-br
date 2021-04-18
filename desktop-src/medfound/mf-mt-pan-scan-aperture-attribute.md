---
description: Define a abertura de panorâmica/digitalização, que é a 4&\# 215; 3 região de vídeo que deve ser exibida no modo de panorâmica/digitalização.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Atributo MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781345"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="127ac-103">\_Atributo de \_ \_ abertura de digitalização de Pan MT MF \_</span><span class="sxs-lookup"><span data-stu-id="127ac-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="127ac-104">Define a abertura de panorâmica/digitalização, que é a área de vídeo de 4 × 3 que deve ser exibida no modo de panorâmica/digitalização.</span><span class="sxs-lookup"><span data-stu-id="127ac-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="127ac-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="127ac-105">Data type</span></span>

<span data-ttu-id="127ac-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="127ac-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="127ac-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="127ac-107">Remarks</span></span>

<span data-ttu-id="127ac-108">O valor do atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="127ac-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="127ac-109">Esse atributo é usado para cortar o vídeo widescreen em uma taxa de proporção de 4:3.</span><span class="sxs-lookup"><span data-stu-id="127ac-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="127ac-110">A abertura de panorâmica/verificação é usada somente no modo de panorâmica/digitalização, que é habilitado definindo o atributo [**MF de \_ \_ Pan \_ \_ MT**](mf-mt-pan-scan-enabled-attribute.md) para **true**.</span><span class="sxs-lookup"><span data-stu-id="127ac-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="127ac-111">Se o modo de panorâmica/verificação não estiver habilitado, use a abertura de exibição, especificada pelo atributo de [**\_ \_ \_ \_ abertura de exibição mínima de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="127ac-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="127ac-112">Se esse atributo não for definido, a abertura de panorâmica/verificação será considerada como o quadro de vídeo inteiro.</span><span class="sxs-lookup"><span data-stu-id="127ac-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="127ac-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="127ac-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="127ac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="127ac-114">Requirements</span></span>



| <span data-ttu-id="127ac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="127ac-115">Requirement</span></span> | <span data-ttu-id="127ac-116">Valor</span><span class="sxs-lookup"><span data-stu-id="127ac-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="127ac-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="127ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="127ac-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="127ac-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="127ac-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="127ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="127ac-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="127ac-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="127ac-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="127ac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="127ac-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="127ac-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127ac-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="127ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127ac-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="127ac-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="127ac-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="127ac-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="127ac-126">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="127ac-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="127ac-127">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="127ac-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="127ac-128">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="127ac-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="127ac-129">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="127ac-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="127ac-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="127ac-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="127ac-131">**\_ \_ abertura geométrica do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="127ac-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="127ac-132">**\_abertura de \_ \_ exibição mínima \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="127ac-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="127ac-133">**\_exame de Pan MT do MF \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="127ac-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




