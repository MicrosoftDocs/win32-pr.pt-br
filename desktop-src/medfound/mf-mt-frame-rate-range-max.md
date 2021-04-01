---
description: A taxa máxima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Atributo MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921268"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="f212d-103">\_ \_ \_ \_ Atributo máximo do intervalo de taxa de quadros MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f212d-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="f212d-104">A taxa máxima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="f212d-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="f212d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f212d-105">Data type</span></span>

<span data-ttu-id="f212d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f212d-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f212d-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="f212d-107">Get/set</span></span>

<span data-ttu-id="f212d-108">Para obter esse atributo, chame [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="f212d-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="f212d-109">Para definir esse atributo, chame [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="f212d-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="f212d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f212d-110">Remarks</span></span>

<span data-ttu-id="f212d-111">A taxa de quadros é expressa como uma taxa.</span><span class="sxs-lookup"><span data-stu-id="f212d-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="f212d-112">Os bits superiores de 32 do valor do atributo contêm o numerador e os bits 32 inferiores contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="f212d-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="f212d-113">Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1.</span><span class="sxs-lookup"><span data-stu-id="f212d-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="f212d-114">Se o dispositivo de captura relatar uma taxa máxima de quadros, a fonte de mídia definirá esse atributo no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f212d-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="f212d-115">A taxa de quadros mínima é fornecida no [atributo \_ \_ min de \_ \_ intervalo de \_ taxa de quadros MF MT](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="f212d-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="f212d-116">O dispositivo não tem garantia de suporte a cada incremento nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="f212d-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="f212d-117">Para definir a taxa de quadros do dispositivo, primeiro modifique o valor do atributo de [**\_ taxa de \_ quadros \_ MF MT**](mf-mt-frame-rate-attribute.md) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f212d-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="f212d-118">Em seguida, defina o tipo de mídia na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="f212d-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="f212d-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f212d-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f212d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f212d-120">Requirements</span></span>



| <span data-ttu-id="f212d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f212d-121">Requirement</span></span> | <span data-ttu-id="f212d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f212d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f212d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f212d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f212d-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f212d-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f212d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f212d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f212d-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f212d-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f212d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f212d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f212d-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f212d-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f212d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f212d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f212d-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f212d-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f212d-131">Como definir a taxa de quadros de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f212d-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="f212d-132">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="f212d-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="f212d-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f212d-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f212d-134">intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ min</span><span class="sxs-lookup"><span data-stu-id="f212d-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




