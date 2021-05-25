---
description: Constantes de filtragem de textura.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343081"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="c32c9-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="c32c9-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="c32c9-104">Constantes de filtragem de textura.</span><span class="sxs-lookup"><span data-stu-id="c32c9-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c32c9-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="c32c9-105">#define</span></span></td>
<td><span data-ttu-id="c32c9-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c32c9-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="c32c9-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="c32c9-108">O dispositivo dá suporte à filtragem de convolução monocromática.</span><span class="sxs-lookup"><span data-stu-id="c32c9-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="c32c9-109">Esse filtro é representado pelo membro D3DTEXF_CONVOLUTIONMONO do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c32c9-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c32c9-110">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c32c9-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c32c9-111">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c32c9-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="c32c9-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="c32c9-113">O dispositivo dá suporte à filtragem de exemplo de ponto por estágio para ampliar texturas.</span><span class="sxs-lookup"><span data-stu-id="c32c9-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="c32c9-114">O filtro de ampliação de exemplo de ponto é representado pelo D3DTEXF_POINT membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c32c9-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="c32c9-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="c32c9-116">O dispositivo dá suporte à filtragem de interpolação bilinear por estágio para ampliar mipmaps.</span><span class="sxs-lookup"><span data-stu-id="c32c9-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="c32c9-117">O filtro mipmapping de interpolação bilinear é representado pelo D3DTEXF_LINEAR membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c32c9-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="c32c9-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="c32c9-119">O dispositivo dá suporte à filtragem anisoél por estágio para ampliar texturas.</span><span class="sxs-lookup"><span data-stu-id="c32c9-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="c32c9-120">O filtro de ampliação anisuária é representado pelo D3DTEXF_ANISOTROPIC membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c32c9-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="c32c9-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="c32c9-122">O dispositivo dá suporte à filtragem de amostra piramidal por estágio para ampliar texturas.</span><span class="sxs-lookup"><span data-stu-id="c32c9-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="c32c9-123">O filtro de lupa piramidal é representado pelo membro de D3DTEXF_PYRAMIDALQUAD do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c32c9-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="c32c9-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="c32c9-125">O dispositivo dá suporte a filtragem quádrupla gaussiano por estágio para ampliar texturas.</span><span class="sxs-lookup"><span data-stu-id="c32c9-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="c32c9-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="c32c9-127">O dispositivo dá suporte à filtragem de amostra de ponto por estágio para texturas minificar.</span><span class="sxs-lookup"><span data-stu-id="c32c9-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="c32c9-128">O filtro minificação de exemplo de ponto é representado pelo membro D3DTEXF_POINT do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c32c9-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="c32c9-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="c32c9-130">O dispositivo dá suporte à filtragem linear por estágio para texturas minificar.</span><span class="sxs-lookup"><span data-stu-id="c32c9-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="c32c9-131">O filtro minificação linear é representado pelo membro D3DTEXF_LINEAR do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c32c9-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="c32c9-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="c32c9-133">O dispositivo dá suporte à filtragem de anisotropic por estágio para texturas minificar.</span><span class="sxs-lookup"><span data-stu-id="c32c9-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="c32c9-134">O filtro anisotropic minificação é representado pelo membro D3DTEXF_ANISOTROPIC do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c32c9-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="c32c9-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="c32c9-136">O dispositivo dá suporte à filtragem de amostra piramidal por estágio para texturas minificar.</span><span class="sxs-lookup"><span data-stu-id="c32c9-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="c32c9-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="c32c9-138">O dispositivo dá suporte à filtragem quádrupla gaussiano por etapa para texturas minificars.</span><span class="sxs-lookup"><span data-stu-id="c32c9-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c32c9-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="c32c9-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="c32c9-140">O dispositivo dá suporte à filtragem de amostra de ponto por etapa para mipmaps.</span><span class="sxs-lookup"><span data-stu-id="c32c9-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="c32c9-141">O filtro mipmapping de exemplo de ponto é representado pelo membro D3DTEXF_POINT do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c32c9-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c32c9-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="c32c9-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="c32c9-143">O dispositivo dá suporte à filtragem de interpolação bilinear por estágio para mipmaps.</span><span class="sxs-lookup"><span data-stu-id="c32c9-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="c32c9-144">O filtro mipmapping de interpolação bilinear é representado pelo D3DTEXF_LINEAR membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="c32c9-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c32c9-145">Essas constantes são usadas pelos membros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="c32c9-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c32c9-146">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="c32c9-146">Constant Information</span></span>



|  <span data-ttu-id="c32c9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32c9-147">Requirement</span></span>                        | <span data-ttu-id="c32c9-148">Valor</span><span class="sxs-lookup"><span data-stu-id="c32c9-148">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c32c9-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c32c9-149">Header</span></span>                   | <span data-ttu-id="c32c9-150">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="c32c9-150">d3d9caps.h</span></span> |
| <span data-ttu-id="c32c9-151">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="c32c9-151">Minimum operating system</span></span> | <span data-ttu-id="c32c9-152">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c32c9-152">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c32c9-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c32c9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c32c9-154">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="c32c9-154">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
