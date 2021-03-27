---
title: Grupos de estado de efeito (Direct3D 11)
description: Os Estados de efeito são pares de valor de nome na forma de uma expressão.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efeito, grupos de estado (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917331"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="278b3-104">Grupos de estado de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="278b3-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="278b3-105">Os Estados de efeito são pares de valor de nome na forma de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="278b3-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="278b3-106">Estado do Blend</span><span class="sxs-lookup"><span data-stu-id="278b3-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="278b3-107">Profundidade e estado do estêncil</span><span class="sxs-lookup"><span data-stu-id="278b3-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="278b3-108">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="278b3-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="278b3-109">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="278b3-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="278b3-110">Estado do objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="278b3-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="278b3-111">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="278b3-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="278b3-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="278b3-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="278b3-113">Estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="278b3-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="278b3-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="278b3-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="278b3-115">Membros de [ **D3D11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="278b3-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="278b3-116">Profundidade e estado do estêncil</span><span class="sxs-lookup"><span data-stu-id="278b3-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="278b3-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="278b3-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="278b3-118">Membros do [ **\_ estêncil de profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="278b3-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="278b3-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="278b3-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="278b3-120">Membro de [ **D3D11 \_ profundidade \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="278b3-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="278b3-121">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="278b3-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="278b3-122">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="278b3-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="278b3-123">**\_Modo de preenchimento D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="278b3-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="278b3-124">De seleção</span><span class="sxs-lookup"><span data-stu-id="278b3-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="278b3-125">**\_Modo de seleção de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="278b3-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="278b3-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="278b3-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="278b3-127">Membros do [ **\_ rasterizador D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="278b3-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="278b3-128">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="278b3-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="278b3-129">Filter endereçou AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="278b3-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="278b3-130">Membros de [ **amostra de D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="278b3-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="278b3-131">Consulte [tipo de amostra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obter exemplos.</span><span class="sxs-lookup"><span data-stu-id="278b3-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="278b3-132">Estado do objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="278b3-132">Effect Object State</span></span>



| <span data-ttu-id="278b3-133">Este objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="278b3-133">This Effect Object</span></span>                          | <span data-ttu-id="278b3-134">É mapeada para</span><span class="sxs-lookup"><span data-stu-id="278b3-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="278b3-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="278b3-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="278b3-136">Um objeto de estado de [estado do rasterizador](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="278b3-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="278b3-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="278b3-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="278b3-138">Um objeto de estado de [estado de profundidade e de estêncil](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="278b3-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="278b3-139">BLENDstate</span><span class="sxs-lookup"><span data-stu-id="278b3-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="278b3-140">Um objeto de estado de [estado de mistura](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="278b3-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="278b3-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="278b3-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="278b3-142">Um objeto de sombreador de vértice compilado.</span><span class="sxs-lookup"><span data-stu-id="278b3-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="278b3-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="278b3-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="278b3-144">Um objeto de sombreador de pixel compilado.</span><span class="sxs-lookup"><span data-stu-id="278b3-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="278b3-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="278b3-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="278b3-146">Um objeto de sombreador Geometry compilado.</span><span class="sxs-lookup"><span data-stu-id="278b3-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="278b3-147">\_SAMPLEMASK DS STENCILREFAB \_ BLENDFACTORAB \_</span><span class="sxs-lookup"><span data-stu-id="278b3-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="278b3-148">Membros de [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="278b3-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="278b3-149">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="278b3-149">Defining and using state objects</span></span>

<span data-ttu-id="278b3-150">Os objetos de estado são declarados em arquivos FX no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="278b3-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="278b3-151">StateObjectType é um dos Estados listados acima e MemberName é o nome de qualquer membro que terá um valor não padrão.</span><span class="sxs-lookup"><span data-stu-id="278b3-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="278b3-152">Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false** , o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="278b3-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="278b3-153">O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="278b3-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="278b3-154">Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="278b3-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="278b3-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="278b3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278b3-156">Sintaxe da técnica de efeito</span><span class="sxs-lookup"><span data-stu-id="278b3-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="278b3-157">Formato de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="278b3-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 