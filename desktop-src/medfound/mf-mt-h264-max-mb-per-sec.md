---
description: Especifica a taxa máxima de processamento de macrobloco para um fluxo de vídeo H. 264.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: Atributo MF_MT_H264_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796062"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a><span data-ttu-id="4993e-103">Atributo do MF \_ MT \_ H264 no \_ máximo \_ MB \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="4993e-103">MF\_MT\_H264\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="4993e-104">Especifica a taxa máxima de processamento de macrobloco para um fluxo de vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="4993e-104">Specifies the maximum macroblock processing rate for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4993e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4993e-105">Data type</span></span>

<span data-ttu-id="4993e-106">**\[ UINT32 \]** armazenado como **UINT8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4993e-106">**UINT32\[\]** stored as **UINT8\[\]**</span></span>

## <a name="applies-to"></a><span data-ttu-id="4993e-107">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="4993e-107">Applies to</span></span>

[<span data-ttu-id="4993e-108">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4993e-108">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="4993e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4993e-109">Remarks</span></span>

<span data-ttu-id="4993e-110">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="4993e-110">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="4993e-111">O valor do atributo é uma matriz de valores UINT32, que correspondem aos campos a seguir no descritor de formato de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="4993e-111">The value of the attribute is an array of UINT32 values, which correspond to the following fields in the UVC 1.5 H.264 video format descriptor.</span></span>

| <span data-ttu-id="4993e-112">Elemento de matriz</span><span class="sxs-lookup"><span data-stu-id="4993e-112">Array Element</span></span> | <span data-ttu-id="4993e-113">Campo de descritor</span><span class="sxs-lookup"><span data-stu-id="4993e-113">Descriptor Field</span></span>                                           |
|---------------|------------------------------------------------------------|
| <span data-ttu-id="4993e-114">0</span><span class="sxs-lookup"><span data-stu-id="4993e-114">0</span></span>             | <span data-ttu-id="4993e-115">**dwMaxMBperSecOneResolutionNoScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-115">**dwMaxMBperSecOneResolutionNoScalability**</span></span>                |
| <span data-ttu-id="4993e-116">1</span><span class="sxs-lookup"><span data-stu-id="4993e-116">1</span></span>             | <span data-ttu-id="4993e-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-117">**dwMaxMBperSecTwoResolutionsNoScalability**</span></span>               |
| <span data-ttu-id="4993e-118">2</span><span class="sxs-lookup"><span data-stu-id="4993e-118">2</span></span>             | <span data-ttu-id="4993e-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-119">**dwMaxMBperSecThreeResolutionsNoScalability**</span></span>             |
| <span data-ttu-id="4993e-120">3</span><span class="sxs-lookup"><span data-stu-id="4993e-120">3</span></span>             | <span data-ttu-id="4993e-121">**dwMaxMBperSecFourResolutionsNoScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-121">**dwMaxMBperSecFourResolutionsNoScalability**</span></span>              |
| <span data-ttu-id="4993e-122">4</span><span class="sxs-lookup"><span data-stu-id="4993e-122">4</span></span>             | <span data-ttu-id="4993e-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-123">**dwMaxMBperSecOneResolutionTemporalScalability**</span></span>          |
| <span data-ttu-id="4993e-124">5</span><span class="sxs-lookup"><span data-stu-id="4993e-124">5</span></span>             | <span data-ttu-id="4993e-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span><span class="sxs-lookup"><span data-stu-id="4993e-125">**dwMaxMBperSecTwoResolutionsTemporalScalablility**</span></span>        |
| <span data-ttu-id="4993e-126">6</span><span class="sxs-lookup"><span data-stu-id="4993e-126">6</span></span>             | <span data-ttu-id="4993e-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-127">**dwMaxMBperSecThreeResolutionsTemporalScalability**</span></span>       |
| <span data-ttu-id="4993e-128">7</span><span class="sxs-lookup"><span data-stu-id="4993e-128">7</span></span>             | <span data-ttu-id="4993e-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-129">**dwMaxMBperSecFourResolutionsTemporalScalability**</span></span>        |
| <span data-ttu-id="4993e-130">8</span><span class="sxs-lookup"><span data-stu-id="4993e-130">8</span></span>             | <span data-ttu-id="4993e-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-131">**dwMaxMBperSecOneResolutionTemporalQualityScalability**</span></span>   |
| <span data-ttu-id="4993e-132">9</span><span class="sxs-lookup"><span data-stu-id="4993e-132">9</span></span>             | <span data-ttu-id="4993e-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-133">**dwMaxMBperSecTwoResolutionsTemporalQualityScalability**</span></span>  |
| <span data-ttu-id="4993e-134">10</span><span class="sxs-lookup"><span data-stu-id="4993e-134">10</span></span>            | <span data-ttu-id="4993e-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span><span class="sxs-lookup"><span data-stu-id="4993e-135">**dwMaxMBperSecThreeResolutionsTemporalQualityScalablity**</span></span> |
| <span data-ttu-id="4993e-136">11</span><span class="sxs-lookup"><span data-stu-id="4993e-136">11</span></span>            | <span data-ttu-id="4993e-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-137">**dwMaxMBperSecFourResolutionsTemporalQualityScalability**</span></span> |
| <span data-ttu-id="4993e-138">12</span><span class="sxs-lookup"><span data-stu-id="4993e-138">12</span></span>            | <span data-ttu-id="4993e-139">**dwMaxMBperSecOneResolutionFullScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-139">**dwMaxMBperSecOneResolutionFullScalability**</span></span>              |
| <span data-ttu-id="4993e-140">13</span><span class="sxs-lookup"><span data-stu-id="4993e-140">13</span></span>            | <span data-ttu-id="4993e-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-141">**dwMaxMBperSecTwoResolutionsFullScalability**</span></span>             |
| <span data-ttu-id="4993e-142">14</span><span class="sxs-lookup"><span data-stu-id="4993e-142">14</span></span>            | <span data-ttu-id="4993e-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-143">**dwMaxMBperSecThreeResolutionsFullScalability**</span></span>           |
| <span data-ttu-id="4993e-144">15</span><span class="sxs-lookup"><span data-stu-id="4993e-144">15</span></span>            | <span data-ttu-id="4993e-145">**dwMaxMBperSecFourResolutionsFullScalability**</span><span class="sxs-lookup"><span data-stu-id="4993e-145">**dwMaxMBperSecFourResolutionsFullScalability**</span></span>            |



 

<span data-ttu-id="4993e-146">Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="4993e-146">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4993e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4993e-147">Requirements</span></span>



| <span data-ttu-id="4993e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="4993e-148">Requirement</span></span> | <span data-ttu-id="4993e-149">Valor</span><span class="sxs-lookup"><span data-stu-id="4993e-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4993e-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4993e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="4993e-151">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4993e-151">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4993e-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4993e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="4993e-153">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4993e-153">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4993e-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4993e-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="4993e-155"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4993e-155"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4993e-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="4993e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4993e-157">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4993e-157">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4993e-158">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="4993e-158">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




