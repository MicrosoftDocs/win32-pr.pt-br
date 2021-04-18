---
description: Especifica os primários de cor para um tipo de mídia de vídeo.
ms.assetid: 56f31c1a-b610-4da0-9df4-76e15add672c
title: Atributo MF_MT_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cdf26a3f49c7e2bb3aa0f48c52c9b283edd8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814552"
---
# <a name="mf_mt_video_primaries-attribute"></a><span data-ttu-id="90eff-103">\_Atributo de \_ primários de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="90eff-103">MF\_MT\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="90eff-104">Especifica os primários de cor para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="90eff-104">Specifies the color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="90eff-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="90eff-105">Data type</span></span>

<span data-ttu-id="90eff-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="90eff-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="90eff-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="90eff-107">Remarks</span></span>

<span data-ttu-id="90eff-108">O valor desse atributo é um membro da enumeração [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) .</span><span class="sxs-lookup"><span data-stu-id="90eff-108">The value of this attribute is a member of the [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration.</span></span>

<span data-ttu-id="90eff-109">A enumeração [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) identifica primárias de cores associadas a determinados padrões de vídeo comuns.</span><span class="sxs-lookup"><span data-stu-id="90eff-109">The [**MFVideoPrimaries**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideoprimaries) enumeration identifies color primaries associated with certain common video standards.</span></span> <span data-ttu-id="90eff-110">Se o tipo de mídia usar primárias de cor que não são identificadas na enumeração **MFVideoPrimaries** , defina o atributo de [**\_ \_ \_ \_ primários de vídeo de MF MT**](mf-mt-custom-video-primaries-attribute.md) em vez desse atributo.</span><span class="sxs-lookup"><span data-stu-id="90eff-110">If the media type uses color primaries that are not identified in the **MFVideoPrimaries** enumeration, set the [**MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES**](mf-mt-custom-video-primaries-attribute.md) attribute instead of this attribute.</span></span>

<span data-ttu-id="90eff-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="90eff-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="90eff-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90eff-112">Requirements</span></span>



| <span data-ttu-id="90eff-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="90eff-113">Requirement</span></span> | <span data-ttu-id="90eff-114">Valor</span><span class="sxs-lookup"><span data-stu-id="90eff-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90eff-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90eff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="90eff-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="90eff-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="90eff-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90eff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="90eff-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="90eff-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="90eff-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90eff-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90eff-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90eff-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90eff-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="90eff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90eff-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90eff-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="90eff-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="90eff-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="90eff-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="90eff-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="90eff-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="90eff-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="90eff-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="90eff-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="90eff-127">Informações de cores estendidas</span><span class="sxs-lookup"><span data-stu-id="90eff-127">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




