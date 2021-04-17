---
description: O número máximo de quadros que o codificador H. 264 leva para responder a um comando.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: Atributo MF_MT_H264_MAX_CODEC_CONFIG_DELAY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754859"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a><span data-ttu-id="fdd04-103">\_Atributo de atraso de configuração de codec MF MT \_ H264 \_ Max \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fdd04-103">MF\_MT\_H264\_MAX\_CODEC\_CONFIG\_DELAY attribute</span></span>

<span data-ttu-id="fdd04-104">O número máximo de quadros que o codificador H. 264 leva para responder a um comando.</span><span class="sxs-lookup"><span data-stu-id="fdd04-104">The maximum number of frames the H.264 encoder takes to respond to a command.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdd04-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fdd04-105">Data type</span></span>

<span data-ttu-id="fdd04-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fdd04-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="fdd04-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="fdd04-107">Get/set</span></span>

<span data-ttu-id="fdd04-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="fdd04-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="fdd04-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="fdd04-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="fdd04-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="fdd04-110">Applies to</span></span>

[<span data-ttu-id="fdd04-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="fdd04-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="fdd04-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd04-112">Remarks</span></span>

<span data-ttu-id="fdd04-113">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="fdd04-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="fdd04-114">O valor corresponde ao campo **bMaxCodecConfigDelay** no descritor de formato de vídeo UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="fdd04-114">The value corresponds to the **bMaxCodecConfigDelay** field in the UVC 1.2 H.264 video format descriptor.</span></span>

<span data-ttu-id="fdd04-115">Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="fdd04-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd04-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd04-116">Requirements</span></span>



| <span data-ttu-id="fdd04-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd04-117">Requirement</span></span> | <span data-ttu-id="fdd04-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fdd04-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd04-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd04-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd04-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdd04-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fdd04-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd04-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd04-122">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdd04-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fdd04-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdd04-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd04-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd04-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdd04-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdd04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd04-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fdd04-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdd04-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="fdd04-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




