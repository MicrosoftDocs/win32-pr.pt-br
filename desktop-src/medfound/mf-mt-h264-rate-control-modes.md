---
description: Especifica o modo de controle de taxa para um fluxo de vídeo H. 264.
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: Atributo MF_MT_H264_RATE_CONTROL_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3fc19070cd3b45aa25a1307a216f611dce1fd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764297"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a><span data-ttu-id="9ed93-103">Atributo de modo de controle de taxa do MF \_ MT \_ H264 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ed93-103">MF\_MT\_H264\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="9ed93-104">Especifica o modo de controle de taxa para um fluxo de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="9ed93-104">Specifies the rate-control mode for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="9ed93-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9ed93-105">Data type</span></span>

<span data-ttu-id="9ed93-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9ed93-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9ed93-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="9ed93-107">Get/set</span></span>

<span data-ttu-id="9ed93-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9ed93-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9ed93-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9ed93-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9ed93-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="9ed93-110">Applies to</span></span>

[<span data-ttu-id="9ed93-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="9ed93-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="9ed93-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ed93-112">Remarks</span></span>

<span data-ttu-id="9ed93-113">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="9ed93-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="9ed93-114">O valor corresponde ao campo **bmRateControlModes** no controle de teste/confirmação UVC 1,2 H. 264.</span><span class="sxs-lookup"><span data-stu-id="9ed93-114">The value corresponds to the **bmRateControlModes** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed93-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ed93-115">Requirements</span></span>



| <span data-ttu-id="9ed93-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed93-116">Requirement</span></span> | <span data-ttu-id="9ed93-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9ed93-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed93-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed93-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed93-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9ed93-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9ed93-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ed93-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed93-121">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9ed93-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9ed93-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ed93-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed93-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ed93-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed93-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ed93-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed93-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ed93-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ed93-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="9ed93-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




