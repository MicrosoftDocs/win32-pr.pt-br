---
description: Indica se um quadro de vídeo é entrelaçado ou progressivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Atributo MFSampleExtension_Interlaced (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780708"
---
# <a name="mfsampleextension_interlaced-attribute"></a><span data-ttu-id="feb39-103">\_Atributo entrelaçado MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="feb39-103">MFSampleExtension\_Interlaced attribute</span></span>

<span data-ttu-id="feb39-104">Indica se um quadro de vídeo é entrelaçado ou progressivo.</span><span class="sxs-lookup"><span data-stu-id="feb39-104">Indicates whether a video frame is interlaced or progressive.</span></span> <span data-ttu-id="feb39-105">Se for **true**, o quadro será entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="feb39-105">If **TRUE**, the frame is interlaced.</span></span> <span data-ttu-id="feb39-106">Se for **false**, o quadro será progressivo.</span><span class="sxs-lookup"><span data-stu-id="feb39-106">If **FALSE**, the frame is progressive.</span></span> <span data-ttu-id="feb39-107">Se não estiver definido, o tipo de mídia descreverá o entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="feb39-107">If not set, the media type describes the interlacing.</span></span> <span data-ttu-id="feb39-108">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="feb39-108">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="feb39-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="feb39-109">Data type</span></span>

<span data-ttu-id="feb39-110">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="feb39-110">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="feb39-111">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="feb39-111">Get/set</span></span>

<span data-ttu-id="feb39-112">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="feb39-112">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="feb39-113">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="feb39-113">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="feb39-114">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="feb39-114">Applies to</span></span>

[<span data-ttu-id="feb39-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="feb39-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="feb39-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb39-116">Remarks</span></span>

<span data-ttu-id="feb39-117">Para conteúdo de vídeo que contém quadros progressivos e entrelaçados mistos, defina o tipo de mídia como entrelaçado e use esse atributo em cada quadro para indicar se o quadro é progressivo ou entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="feb39-117">For video content that contains mixed progressive and interlaced frames, set the media type to interlaced and use this attribute on each frame to indicate whether the frame is progressive or interlaced.</span></span>

<span data-ttu-id="feb39-118">Para conteúdo de vídeo totalmente entrelaçado, defina o tipo de mídia como entrelaçado e omita esse atributo ou defina-o como **verdadeiro** em cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="feb39-118">For video content that is entirely interlaced, set the media type to interlaced and omit this attribute, or set it to **TRUE** on every sample.</span></span>

<span data-ttu-id="feb39-119">Para conteúdo de vídeo totalmente progressivo, defina o tipo de mídia como progressivo e omita esse atributo ou defina-o como **false** em cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="feb39-119">For video content that is entirely progressive, set the media type to progressive and omit this attribute, or set it to **FALSE** on every sample.</span></span>

<span data-ttu-id="feb39-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="feb39-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb39-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb39-121">Requirements</span></span>



| <span data-ttu-id="feb39-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb39-122">Requirement</span></span> | <span data-ttu-id="feb39-123">Valor</span><span class="sxs-lookup"><span data-stu-id="feb39-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="feb39-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb39-124">Minimum supported client</span></span><br/> | <span data-ttu-id="feb39-125">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="feb39-125">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="feb39-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb39-126">Minimum supported server</span></span><br/> | <span data-ttu-id="feb39-127">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="feb39-127">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="feb39-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="feb39-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb39-129"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb39-129"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb39-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="feb39-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb39-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="feb39-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="feb39-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="feb39-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="feb39-133">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="feb39-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="feb39-134">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="feb39-134">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="feb39-135">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="feb39-135">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="feb39-136">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="feb39-136">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="feb39-137">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="feb39-137">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




