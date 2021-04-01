---
description: Ajusta as características de cor de um fluxo de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: DSP de transformação de controle de cores (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646611"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="adf4c-103">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="adf4c-103">Color Control Transform DSP</span></span>

<span data-ttu-id="adf4c-104">Ajusta as características de cor de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="adf4c-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="adf4c-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="adf4c-105">CLSID</span></span>

<span data-ttu-id="adf4c-106">\_CCOLORCONTROLDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="adf4c-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="adf4c-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="adf4c-107">Interfaces</span></span>

-   <span data-ttu-id="adf4c-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="adf4c-108">**IMediaObject**</span></span>
-   <span data-ttu-id="adf4c-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="adf4c-109">**IMFTransform**</span></span>
-   <span data-ttu-id="adf4c-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="adf4c-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="adf4c-111">Formatos</span><span class="sxs-lookup"><span data-stu-id="adf4c-111">Formats</span></span>

-   <span data-ttu-id="adf4c-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="adf4c-112">RGB 24</span></span>
-   <span data-ttu-id="adf4c-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="adf4c-113">RGB 32</span></span>
-   <span data-ttu-id="adf4c-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="adf4c-114">RGB 555</span></span>
-   <span data-ttu-id="adf4c-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="adf4c-115">RGB 565</span></span>
-   <span data-ttu-id="adf4c-116">AYUV</span><span class="sxs-lookup"><span data-stu-id="adf4c-116">AYUV</span></span>
-   <span data-ttu-id="adf4c-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="adf4c-117">UYVY</span></span>
-   <span data-ttu-id="adf4c-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="adf4c-118">YUY2</span></span>
-   <span data-ttu-id="adf4c-119">YV12</span><span class="sxs-lookup"><span data-stu-id="adf4c-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="adf4c-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="adf4c-120">Properties</span></span>

-   [<span data-ttu-id="adf4c-121">\_brilho da cor do MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="adf4c-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="adf4c-122">\_contraste de cor do MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="adf4c-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="adf4c-123">\_matiz de cor de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="adf4c-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="adf4c-124">\_saturação de cor MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="adf4c-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="adf4c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="adf4c-125">Remarks</span></span>

<span data-ttu-id="adf4c-126">Esse DSP modifica o conteúdo do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="adf4c-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="adf4c-127">Para reprodução, você pode conseguir efeitos semelhantes com mais eficiência usando a interface **IMFVideoProcessor** , que controla o processamento de vídeo na placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="adf4c-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf4c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf4c-128">Requirements</span></span>



| <span data-ttu-id="adf4c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf4c-129">Requirement</span></span> | <span data-ttu-id="adf4c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="adf4c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf4c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf4c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="adf4c-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adf4c-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="adf4c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf4c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="adf4c-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="adf4c-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adf4c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adf4c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf4c-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf4c-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="adf4c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="adf4c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf4c-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf4c-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="adf4c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf4c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf4c-140">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="adf4c-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




