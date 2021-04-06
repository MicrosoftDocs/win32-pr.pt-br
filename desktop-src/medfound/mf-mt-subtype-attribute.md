---
description: GUID de subtipo para um tipo de mídia.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Atributo MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011097"
---
# <a name="mf_mt_subtype-attribute"></a><span data-ttu-id="6daaa-103">\_Atributo de \_ subtipo MF MT</span><span class="sxs-lookup"><span data-stu-id="6daaa-103">MF\_MT\_SUBTYPE attribute</span></span>

<span data-ttu-id="6daaa-104">GUID de subtipo para um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="6daaa-104">Subtype GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6daaa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6daaa-105">Data type</span></span>

<span data-ttu-id="6daaa-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6daaa-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="6daaa-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6daaa-107">Remarks</span></span>

<span data-ttu-id="6daaa-108">O GUID de subtipo define um tipo de formato de mídia específico dentro de um tipo principal.</span><span class="sxs-lookup"><span data-stu-id="6daaa-108">The subtype GUID defines a specific media format type within a major type.</span></span> <span data-ttu-id="6daaa-109">Por exemplo, no vídeo, os subtipos incluem RGB-24, RGB-32, UYVY, AYUV e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6daaa-109">For example, within video, the subtypes include RGB-24, RGB-32, UYVY, AYUV, and so forth.</span></span> <span data-ttu-id="6daaa-110">No áudio, os subtipos incluem áudio PCM, áudio do Windows Media 9 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6daaa-110">Within audio, the subtypes include PCM audio, Windows Media Audio 9, and so forth.</span></span>

<span data-ttu-id="6daaa-111">Para obter os valores possíveis, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6daaa-111">For possible values, see the following topics:</span></span>

-   [<span data-ttu-id="6daaa-112">GUIDs de subtipo de áudio</span><span class="sxs-lookup"><span data-stu-id="6daaa-112">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
-   [<span data-ttu-id="6daaa-113">GUIDs de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="6daaa-113">Video Subtype GUIDs</span></span>](video-subtype-guids.md)

<span data-ttu-id="6daaa-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6daaa-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6daaa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6daaa-115">Requirements</span></span>



| <span data-ttu-id="6daaa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6daaa-116">Requirement</span></span> | <span data-ttu-id="6daaa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6daaa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6daaa-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6daaa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6daaa-119">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="6daaa-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6daaa-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6daaa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6daaa-121">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6daaa-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6daaa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6daaa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6daaa-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6daaa-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6daaa-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6daaa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6daaa-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6daaa-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6daaa-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="6daaa-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="6daaa-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="6daaa-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="6daaa-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6daaa-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6daaa-129">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="6daaa-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




