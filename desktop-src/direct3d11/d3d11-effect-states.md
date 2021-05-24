---
title: Grupos de estado de efeito (Direct3D 11)
description: Os Estados de efeito são pares de valor de nome na forma de uma expressão.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efeito, grupos de estado (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335330"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="8e2f4-104">Grupos de estado de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="8e2f4-105">Os Estados de efeito são pares de valor de nome na forma de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="8e2f4-106">Estado do Blend</span><span class="sxs-lookup"><span data-stu-id="8e2f4-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="8e2f4-107">Profundidade e estado do estêncil</span><span class="sxs-lookup"><span data-stu-id="8e2f4-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="8e2f4-108">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="8e2f4-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="8e2f4-109">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="8e2f4-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="8e2f4-110">Estado do objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="8e2f4-111">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="8e2f4-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="8e2f4-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e2f4-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="8e2f4-113">Estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="8e2f4-113">Blend State</span></span>



| <span data-ttu-id="8e2f4-114">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="8e2f4-115">Grupo</span><span class="sxs-lookup"><span data-stu-id="8e2f4-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="8e2f4-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="8e2f4-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="8e2f4-117">Membros de [ **D3D11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="8e2f4-118">Profundidade e estado do estêncil</span><span class="sxs-lookup"><span data-stu-id="8e2f4-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="8e2f4-119">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="8e2f4-120">Grupo</span><span class="sxs-lookup"><span data-stu-id="8e2f4-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8e2f4-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="8e2f4-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="8e2f4-122">Membros do [ **\_ estêncil de profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="8e2f4-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="8e2f4-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="8e2f4-124">Membro de [ **D3D11 \_ profundidade \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="8e2f4-125">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="8e2f4-125">Rasterizer State</span></span>



| <span data-ttu-id="8e2f4-126">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="8e2f4-127">Grupo</span><span class="sxs-lookup"><span data-stu-id="8e2f4-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e2f4-128">Fillmode</span><span class="sxs-lookup"><span data-stu-id="8e2f4-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="8e2f4-129">**MODO DE PREENCHIMENTO D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8e2f4-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="8e2f4-130">MODELO DE RESLÚSCULO</span><span class="sxs-lookup"><span data-stu-id="8e2f4-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="8e2f4-131">**MODO DE \_ RESSADA D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="8e2f4-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="8e2f4-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSCALEDDEPTHBIAS ZCLIPENABLESCSUBSTABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="8e2f4-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="8e2f4-133">Membros do [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="8e2f4-134">Estado do sampler</span><span class="sxs-lookup"><span data-stu-id="8e2f4-134">Sampler State</span></span>



| <span data-ttu-id="8e2f4-135">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="8e2f4-136">Grupo</span><span class="sxs-lookup"><span data-stu-id="8e2f4-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8e2f4-137">Endereço de filtroDados da addressVW MipLODBias MaxAnosoavoy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="8e2f4-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="8e2f4-138">Membros do [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="8e2f4-139">Consulte [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para ver exemplos.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="8e2f4-140">Estado do objeto Effect</span><span class="sxs-lookup"><span data-stu-id="8e2f4-140">Effect Object State</span></span>



| <span data-ttu-id="8e2f4-141">Este objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-141">This Effect Object</span></span>                          | <span data-ttu-id="8e2f4-142">É mapeada para</span><span class="sxs-lookup"><span data-stu-id="8e2f4-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8e2f4-143">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="8e2f4-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="8e2f4-144">Um objeto de estado de Estado do [Rasterizer.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="8e2f4-145">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="8e2f4-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="8e2f4-146">Um [objeto de estado De profundidade e estêncil.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="8e2f4-147">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="8e2f4-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="8e2f4-148">Um [objeto de estado do Blend State.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="8e2f4-149">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="8e2f4-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="8e2f4-150">Um objeto de sombreador de vértice compilado.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="8e2f4-151">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="8e2f4-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="8e2f4-152">Um objeto de sombreador de pixel compilado.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="8e2f4-153">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="8e2f4-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="8e2f4-154">Um objeto de sombreador Geometry compilado.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="8e2f4-155">\_SAMPLEMASK DS STENCILREFAB \_ BLENDFACTORAB \_</span><span class="sxs-lookup"><span data-stu-id="8e2f4-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="8e2f4-156">Membros de [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f4-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="8e2f4-157">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="8e2f4-157">Defining and using state objects</span></span>

<span data-ttu-id="8e2f4-158">Os objetos de estado são declarados em arquivos FX no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="8e2f4-159">StateObjectType é um dos Estados listados acima e MemberName é o nome de qualquer membro que terá um valor não padrão.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="8e2f4-160">Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false** , o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="8e2f4-161">O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f4-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="8e2f4-162">Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="8e2f4-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="8e2f4-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e2f4-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e2f4-164">Sintaxe da técnica de efeito</span><span class="sxs-lookup"><span data-stu-id="8e2f4-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="8e2f4-165">Formato de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="8e2f4-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 