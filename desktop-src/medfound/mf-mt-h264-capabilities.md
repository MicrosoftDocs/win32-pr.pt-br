---
description: Especifica os sinalizadores de recursos para um fluxo de vídeo H. 264.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: Atributo MF_MT_H264_CAPABILITIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67f796e09d4b57667a3d8f7c7c0fa888eba7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837156"
---
# <a name="mf_mt_h264_capabilities-attribute"></a><span data-ttu-id="931c3-103">Atributo de recursos do MF \_ MT \_ H264 \_</span><span class="sxs-lookup"><span data-stu-id="931c3-103">MF\_MT\_H264\_CAPABILITIES attribute</span></span>

<span data-ttu-id="931c3-104">Especifica os sinalizadores de recursos para um fluxo de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="931c3-104">Specifies the capabilities flags for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="931c3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="931c3-105">Data type</span></span>

<span data-ttu-id="931c3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="931c3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="931c3-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="931c3-107">Get/set</span></span>

<span data-ttu-id="931c3-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="931c3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="931c3-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="931c3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="931c3-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="931c3-110">Applies to</span></span>

[<span data-ttu-id="931c3-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="931c3-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="931c3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="931c3-112">Remarks</span></span>

<span data-ttu-id="931c3-113">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="931c3-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="931c3-114">O valor corresponde ao campo **bmCapabilities** no descritor de quadro de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="931c3-114">The value corresponds to the **bmCapabilities** field in the UVC 1.5 H.264 video frame descriptor.</span></span>

<span data-ttu-id="931c3-115">Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="931c3-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="931c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="931c3-116">Requirements</span></span>



| <span data-ttu-id="931c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="931c3-117">Requirement</span></span> | <span data-ttu-id="931c3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="931c3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="931c3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="931c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="931c3-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="931c3-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="931c3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="931c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="931c3-122">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="931c3-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="931c3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="931c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="931c3-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="931c3-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="931c3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="931c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="931c3-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="931c3-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="931c3-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="931c3-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




