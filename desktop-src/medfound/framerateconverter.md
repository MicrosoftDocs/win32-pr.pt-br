---
description: Altera a taxa de quadros de um fluxo de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Conversor de taxa de quadros DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646582"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="62297-103">Conversor de taxa de quadros DSP</span><span class="sxs-lookup"><span data-stu-id="62297-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="62297-104">Altera a taxa de quadros de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62297-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="62297-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="62297-105">CLSID</span></span>

<span data-ttu-id="62297-106">\_CFRAMERATECONVERTDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="62297-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="62297-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="62297-107">Interfaces</span></span>

-   <span data-ttu-id="62297-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="62297-108">**IMediaObject**</span></span>
-   <span data-ttu-id="62297-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="62297-109">**IMFTransform**</span></span>
-   <span data-ttu-id="62297-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="62297-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="62297-111">Formatos</span><span class="sxs-lookup"><span data-stu-id="62297-111">Formats</span></span>

-   <span data-ttu-id="62297-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="62297-112">ARGB 32</span></span>
-   <span data-ttu-id="62297-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="62297-113">RGB 24</span></span>
-   <span data-ttu-id="62297-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="62297-114">RGB 32</span></span>
-   <span data-ttu-id="62297-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="62297-115">RGB 555</span></span>
-   <span data-ttu-id="62297-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="62297-116">RGB 565</span></span>
-   <span data-ttu-id="62297-117">AYUV</span><span class="sxs-lookup"><span data-stu-id="62297-117">AYUV</span></span>
-   <span data-ttu-id="62297-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="62297-118">IYUV</span></span>
-   <span data-ttu-id="62297-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="62297-119">UYVY</span></span>
-   <span data-ttu-id="62297-120">Y211</span><span class="sxs-lookup"><span data-stu-id="62297-120">Y211</span></span>
-   <span data-ttu-id="62297-121">Y411</span><span class="sxs-lookup"><span data-stu-id="62297-121">Y411</span></span>
-   <span data-ttu-id="62297-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="62297-122">Y41P</span></span>
-   <span data-ttu-id="62297-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="62297-123">YUY2</span></span>
-   <span data-ttu-id="62297-124">YUYV</span><span class="sxs-lookup"><span data-stu-id="62297-124">YUYV</span></span>
-   <span data-ttu-id="62297-125">YV12</span><span class="sxs-lookup"><span data-stu-id="62297-125">YV12</span></span>
-   <span data-ttu-id="62297-126">YVYU</span><span class="sxs-lookup"><span data-stu-id="62297-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="62297-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62297-127">Properties</span></span>

-   [<span data-ttu-id="62297-128">MFPKEY \_ convu \_ INPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="62297-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="62297-129">MFPKEY \_ convu \_ OUTPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="62297-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="62297-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="62297-130">Remarks</span></span>

<span data-ttu-id="62297-131">Esse DSP altera a taxa de quadros repetindo ou soltando quadros.</span><span class="sxs-lookup"><span data-stu-id="62297-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="62297-132">Por padrão, o DSP Obtém as taxas de quadros dos tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="62297-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="62297-133">Opcionalmente, você pode especificar as taxas de quadros definindo as \_ Propriedades MFPKEY CONV \_ INPUTFRAMERATE e MFPKEY \_ CONV \_ OUTPUTFRAMERATE.</span><span class="sxs-lookup"><span data-stu-id="62297-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="62297-134">Esses valores substituem a taxa de quadros fornecida no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="62297-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="62297-135">No entanto, se você estiver usando esse DSP dentro do pipeline de Media Foundation, não deverá definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62297-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="62297-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62297-136">Requirements</span></span>



| <span data-ttu-id="62297-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="62297-137">Requirement</span></span> | <span data-ttu-id="62297-138">Valor</span><span class="sxs-lookup"><span data-stu-id="62297-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62297-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62297-139">Minimum supported client</span></span><br/> | <span data-ttu-id="62297-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62297-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="62297-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62297-141">Minimum supported server</span></span><br/> | <span data-ttu-id="62297-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62297-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62297-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62297-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="62297-144"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62297-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="62297-145">DLL</span><span class="sxs-lookup"><span data-stu-id="62297-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62297-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62297-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62297-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="62297-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62297-148">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="62297-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




