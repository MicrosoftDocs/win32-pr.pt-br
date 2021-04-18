---
description: Redimensiona um fluxo de vídeo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: DSP de redimensionador de vídeo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810698"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="ec713-103">DSP de redimensionador de vídeo</span><span class="sxs-lookup"><span data-stu-id="ec713-103">Video Resizer DSP</span></span>

<span data-ttu-id="ec713-104">Redimensiona um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec713-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="ec713-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec713-105">CLSID</span></span>

<span data-ttu-id="ec713-106">\_CRESIZERDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="ec713-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="ec713-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="ec713-107">Interfaces</span></span>

-   [<span data-ttu-id="ec713-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="ec713-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="ec713-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="ec713-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="ec713-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="ec713-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="ec713-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="ec713-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="ec713-112">**IWMResizerProps**</span><span class="sxs-lookup"><span data-stu-id="ec713-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="ec713-113">Formatos</span><span class="sxs-lookup"><span data-stu-id="ec713-113">Formats</span></span>

<span data-ttu-id="ec713-114">O DSP do redimensionador de vídeo dá suporte aos seguintes subtipos de mídia de entrada/saída quando ele está agindo como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="ec713-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="ec713-115">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="ec713-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="ec713-116">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="ec713-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="ec713-117">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="ec713-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="ec713-118">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="ec713-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="ec713-119">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="ec713-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="ec713-120">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="ec713-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="ec713-121">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="ec713-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="ec713-122">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="ec713-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="ec713-123">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="ec713-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="ec713-124">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="ec713-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="ec713-125">MEDIASUBTYPE \_ V216</span><span class="sxs-lookup"><span data-stu-id="ec713-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="ec713-126">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="ec713-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="ec713-127">O DSP do redimensionador de vídeo dá suporte aos seguintes subtipos de mídia de entrada/saída quando está atuando como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="ec713-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="ec713-128">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="ec713-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="ec713-129">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="ec713-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="ec713-130">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="ec713-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="ec713-131">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="ec713-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="ec713-132">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="ec713-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="ec713-133">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="ec713-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="ec713-134">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="ec713-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="ec713-135">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="ec713-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="ec713-136">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="ec713-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="ec713-137">MFVideoFormat \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="ec713-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="ec713-138">MFVideoFormat \_ V216</span><span class="sxs-lookup"><span data-stu-id="ec713-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="ec713-139">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="ec713-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="ec713-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec713-140">Properties</span></span>

-   [<span data-ttu-id="ec713-141">MFPKEY \_ redimensionar \_ src \_ Left</span><span class="sxs-lookup"><span data-stu-id="ec713-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="ec713-142">MFPKEY \_ redimensionar \_ src \_ superior</span><span class="sxs-lookup"><span data-stu-id="ec713-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="ec713-143">\_largura de src de redimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec713-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="ec713-144">MFPKEY \_ dimensionar \_ altura de src \_</span><span class="sxs-lookup"><span data-stu-id="ec713-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="ec713-145">MFPKEY \_ redimensionar o \_ DST \_ esquerdo</span><span class="sxs-lookup"><span data-stu-id="ec713-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="ec713-146">MFPKEY \_ redimensionar o \_ DST \_ superior</span><span class="sxs-lookup"><span data-stu-id="ec713-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="ec713-147">\_largura de hora de redimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec713-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="ec713-148">MFPKEY \_ redimensionar a \_ altura do horário de verão \_</span><span class="sxs-lookup"><span data-stu-id="ec713-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="ec713-149">\_qualidade de redimensionamento MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="ec713-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="ec713-150">MFPKEY \_ redimensionar \_ entrelaçamento</span><span class="sxs-lookup"><span data-stu-id="ec713-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="ec713-151">MFPKEY \_ redimensionar \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="ec713-152">MFPKEY \_ redimensionar \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="ec713-153">MFPKEY \_ redimensionar \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="ec713-154">MFPKEY \_ redimensionar \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="ec713-155">MFPKEY \_ redimensionar \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="ec713-156">MFPKEY \_ redimensionar \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="ec713-157">MFPKEY \_ redimensionar \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="ec713-158">MFPKEY \_ redimensionar \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="ec713-159">MFPKEY \_ redimensionar \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="ec713-160">MFPKEY \_ redimensionar \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="ec713-161">MFPKEY \_ redimensionar \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="ec713-162">MFPKEY \_ redimensionar \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="ec713-163">MFPKEY \_ PIXELASPECTRATIO</span><span class="sxs-lookup"><span data-stu-id="ec713-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="ec713-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec713-164">Remarks</span></span>

<span data-ttu-id="ec713-165">O DSP do redimensionador de vídeo é implementado como um objeto COM que pode atuar como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="ec713-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="ec713-166">O objeto tem um único identificador de classe (CLSID), independentemente de agir como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="ec713-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="ec713-167">Para obter informações sobre quando um DSP atua como um DMO ou uma MFT, consulte [processadores de sinais digitais](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="ec713-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="ec713-168">Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um DSP está agindo como um DMO ou uma MFT.</span><span class="sxs-lookup"><span data-stu-id="ec713-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="ec713-169">Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um DSP estar agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="ec713-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="ec713-170">Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ec713-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="ec713-171">Esse DSP pode executar o corte e o dimensionamento na imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec713-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="ec713-172">O formato do tipo de saída deve corresponder ao formato do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec713-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="ec713-173">O DSP não executa conversões de espaço em cores.</span><span class="sxs-lookup"><span data-stu-id="ec713-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="ec713-174">Antes de definir o tipo de saída, você pode definir qualquer uma das seguintes regiões usando as propriedades listadas nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="ec713-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="ec713-175">Região</span><span class="sxs-lookup"><span data-stu-id="ec713-175">Region</span></span>                   | <span data-ttu-id="ec713-176">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec713-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec713-177">Retângulo de origem</span><span class="sxs-lookup"><span data-stu-id="ec713-177">Source rectangle</span></span>         | <span data-ttu-id="ec713-178">MFPKEY \_ redimensionar \_ src \_ Left</span><span class="sxs-lookup"><span data-stu-id="ec713-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="ec713-179">MFPKEY \_ redimensionar \_ src \_ superior</span><span class="sxs-lookup"><span data-stu-id="ec713-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="ec713-180">\_largura de src de redimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec713-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="ec713-181">MFPKEY \_ dimensionar \_ altura de src \_</span><span class="sxs-lookup"><span data-stu-id="ec713-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="ec713-182">Retângulo de destino</span><span class="sxs-lookup"><span data-stu-id="ec713-182">Destination rectangle</span></span>    | <span data-ttu-id="ec713-183">MFPKEY \_ redimensionar o \_ DST \_ esquerdo</span><span class="sxs-lookup"><span data-stu-id="ec713-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="ec713-184">MFPKEY \_ redimensionar o \_ DST \_ superior</span><span class="sxs-lookup"><span data-stu-id="ec713-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="ec713-185">\_largura de hora de redimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec713-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="ec713-186">MFPKEY \_ redimensionar a \_ altura do horário de verão \_</span><span class="sxs-lookup"><span data-stu-id="ec713-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="ec713-187">Abertura geométrica</span><span class="sxs-lookup"><span data-stu-id="ec713-187">Geometric aperture</span></span>       | <span data-ttu-id="ec713-188">MFPKEY \_ redimensionar \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="ec713-189">MFPKEY \_ redimensionar \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="ec713-190">MFPKEY \_ redimensionar \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="ec713-191">MFPKEY \_ redimensionar \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="ec713-192">Abertura de exibição mínima</span><span class="sxs-lookup"><span data-stu-id="ec713-192">Minimum display aperture</span></span> | <span data-ttu-id="ec713-193">MFPKEY \_ redimensionar \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="ec713-194">MFPKEY \_ redimensionar \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="ec713-195">MFPKEY \_ redimensionar \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="ec713-196">MFPKEY \_ redimensionar \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="ec713-197">Região de panorâmica/verificação</span><span class="sxs-lookup"><span data-stu-id="ec713-197">Pan/scan region</span></span>          | <span data-ttu-id="ec713-198">MFPKEY \_ redimensionar \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="ec713-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="ec713-199">MFPKEY \_ redimensionar \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="ec713-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="ec713-200">MFPKEY \_ redimensionar \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="ec713-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="ec713-201">MFPKEY \_ redimensionar \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="ec713-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="ec713-202">Em cada caso, você deve definir todas as propriedades associadas para que a configuração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="ec713-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="ec713-203">O DSP copia a parte da imagem de origem definida pelo retângulo de origem e a amplia ou compacta para o retângulo de destino no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="ec713-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="ec713-204">Os retângulos de origem e de destino não precisam ter o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="ec713-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="ec713-205">O tamanho do quadro no tipo de mídia de saída deve ser grande o suficiente para conter o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="ec713-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="ec713-206">A abertura geométrica, a abertura de exibição mínima e a região de panorâmica/verificação não afetam o modo como o DSP redimensiona o vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec713-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="ec713-207">No entanto, eles podem afetar como o componente downstream interpreta o quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec713-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="ec713-208">Em particular, o processador de vídeo avançado (EVR) usa esses valores quando calcula a taxa de proporção da imagem e a área de exibição.</span><span class="sxs-lookup"><span data-stu-id="ec713-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="ec713-209">Se você estiver usando Media Foundation tipos de mídia, poderá definir a abertura geométrica, a abertura de exibição mínima e as regiões de panorâmica/verificação diretamente no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="ec713-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="ec713-210">Caso contrário, se você estiver usando tipos de mídia DMO, defina-os usando as propriedades.</span><span class="sxs-lookup"><span data-stu-id="ec713-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="ec713-211">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="ec713-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ec713-212">**\_ \_ abertura geométrica do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="ec713-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="ec713-213">**\_abertura de \_ \_ exibição mínima \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="ec713-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="ec713-214">**\_abertura de \_ digitalização de Pan MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="ec713-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="ec713-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec713-215">Requirements</span></span>



| <span data-ttu-id="ec713-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec713-216">Requirement</span></span> | <span data-ttu-id="ec713-217">Valor</span><span class="sxs-lookup"><span data-stu-id="ec713-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec713-218">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec713-218">Minimum supported client</span></span><br/> | <span data-ttu-id="ec713-219">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec713-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec713-220">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec713-220">Minimum supported server</span></span><br/> | <span data-ttu-id="ec713-221">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec713-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec713-222">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec713-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec713-223"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec713-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="ec713-224">DLL</span><span class="sxs-lookup"><span data-stu-id="ec713-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec713-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec713-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec713-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec713-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec713-227">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="ec713-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
