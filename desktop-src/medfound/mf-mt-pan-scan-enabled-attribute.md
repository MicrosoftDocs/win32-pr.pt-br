---
description: Especifica se o modo de panorâmica/verificação está habilitado.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Atributo MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505761"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="9157c-103">\_ \_ \_ Atributo habilitado para exame \_ panorâmico do MF MT</span><span class="sxs-lookup"><span data-stu-id="9157c-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="9157c-104">Especifica se o modo de panorâmica/verificação está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9157c-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="9157c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9157c-105">Data type</span></span>

<span data-ttu-id="9157c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9157c-106">**UINT32**</span></span>

<span data-ttu-id="9157c-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="9157c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9157c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9157c-108">Remarks</span></span>

<span data-ttu-id="9157c-109">Se esse atributo for **true**, somente a região de panorâmica/verificação do vídeo deverá ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9157c-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="9157c-110">A região de panorâmica/verificação é especificada pelo atributo de [**\_ abertura de \_ \_ digitalização \_ de Pan MT MF**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9157c-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="9157c-111">Se esse atributo for **false** ou não definido, toda a abertura de tela do vídeo deverá ser exibida.</span><span class="sxs-lookup"><span data-stu-id="9157c-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="9157c-112">A abertura de exibição é especificada pelo atributo de [**\_ \_ \_ \_ abertura de exibição mínima de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9157c-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="9157c-113">Se você definir esse atributo como **true**, defina também o valor do atributo [**de \_ \_ abertura de \_ digitalização \_ de Pan MT MF**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9157c-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="9157c-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9157c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9157c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9157c-115">Requirements</span></span>



| <span data-ttu-id="9157c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9157c-116">Requirement</span></span> | <span data-ttu-id="9157c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9157c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9157c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9157c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9157c-119">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="9157c-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9157c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9157c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9157c-121">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9157c-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9157c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9157c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9157c-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9157c-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9157c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9157c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9157c-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9157c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9157c-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9157c-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9157c-127">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="9157c-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9157c-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="9157c-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="9157c-129">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="9157c-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="9157c-130">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="9157c-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




