---
description: Estados de efeito são pares nome-valor na forma de uma expressão.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335560"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="6125f-103">Grupos de estado de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6125f-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="6125f-104">Estados de efeito são pares nome-valor na forma de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="6125f-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="6125f-105">Estado do Blend</span><span class="sxs-lookup"><span data-stu-id="6125f-105">Blend state</span></span>

| <span data-ttu-id="6125f-106">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-106">Effect state</span></span> | <span data-ttu-id="6125f-107">Grupo</span><span class="sxs-lookup"><span data-stu-id="6125f-107">Group</span></span> |
|-|-|
| <span data-ttu-id="6125f-108">**ALPHATOCOVERAGEENABLE,** **BLENDENABLE,** **SRCBLEND,** **DESTBLEND,** **BLENDOP,** **SRCBLENDALPHA,** **DESTBLENDALPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="6125f-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="6125f-109">Membros do [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="6125f-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="6125f-110">Profundidade e estado de estêncil</span><span class="sxs-lookup"><span data-stu-id="6125f-110">Depth and stencil state</span></span>

| <span data-ttu-id="6125f-111">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-111">Effect state</span></span>| <span data-ttu-id="6125f-112">Grupo</span><span class="sxs-lookup"><span data-stu-id="6125f-112">Group</span></span> |
|-|-|
| <span data-ttu-id="6125f-113">**DEPTHENABLE,** **DEPTHWRITEMASK,** **DEPTHFUNC,NCILENABLE,** **STENCILREADMASK,** **STENCILWRITEMASK** </span><span class="sxs-lookup"><span data-stu-id="6125f-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="6125f-114">Membros do [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="6125f-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="6125f-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="6125f-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="6125f-116">Membro do [ **D3D10 \_ DEPTH \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="6125f-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="6125f-117">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="6125f-117">Rasterizer state</span></span>

| <span data-ttu-id="6125f-118">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-118">Effect state</span></span>| <span data-ttu-id="6125f-119">Grupo</span><span class="sxs-lookup"><span data-stu-id="6125f-119">Group</span></span> |
|-|-|
| <span data-ttu-id="6125f-120">Fillmode</span><span class="sxs-lookup"><span data-stu-id="6125f-120">FILLMODE</span></span> | [<span data-ttu-id="6125f-121">**MODO DE PREENCHIMENTO D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6125f-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="6125f-122">MODELO DE RESLÚSCULO</span><span class="sxs-lookup"><span data-stu-id="6125f-122">CULLMODE</span></span> | [<span data-ttu-id="6125f-123">**MODO DE \_ RESSUÇÃO D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="6125f-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="6125f-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP,** **SLOPESCALEDDEPTHBIAS,** **ZCLIPENABLE,** **SCISSORENABLE,** **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="6125f-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="6125f-125">Membros do [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="6125f-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="6125f-126">Estado de amostra</span><span class="sxs-lookup"><span data-stu-id="6125f-126">Sampler state</span></span>

| <span data-ttu-id="6125f-127">Estado do efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-127">Effect state</span></span> | <span data-ttu-id="6125f-128">Grupo</span><span class="sxs-lookup"><span data-stu-id="6125f-128">Group</span></span> |
|-|-|
| <span data-ttu-id="6125f-129">**Filtro**, **endereçou**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="6125f-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="6125f-130">Membros de [ **amostra de d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="6125f-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="6125f-131">Consulte [tipo de amostra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obter exemplos.</span><span class="sxs-lookup"><span data-stu-id="6125f-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="6125f-132">Estado do objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-132">Effect object state</span></span>

| <span data-ttu-id="6125f-133">Este objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-133">This effect object</span></span> | <span data-ttu-id="6125f-134">É mapeada para</span><span class="sxs-lookup"><span data-stu-id="6125f-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="6125f-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="6125f-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="6125f-136">Um objeto de estado de [estado do rasterizador](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="6125f-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="6125f-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="6125f-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="6125f-138">Um objeto de estado de [estado de profundidade e de estêncil](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="6125f-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="6125f-139">BLENDstate</span><span class="sxs-lookup"><span data-stu-id="6125f-139">BLENDSTATE</span></span> | <span data-ttu-id="6125f-140">Um objeto de estado de [estado de mistura](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="6125f-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="6125f-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="6125f-141">VERTEXSHADER</span></span> | <span data-ttu-id="6125f-142">Um objeto de sombreador de vértice compilado.</span><span class="sxs-lookup"><span data-stu-id="6125f-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="6125f-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="6125f-143">PIXELSHADER</span></span> | <span data-ttu-id="6125f-144">Um objeto de sombreador de pixel compilado.</span><span class="sxs-lookup"><span data-stu-id="6125f-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="6125f-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="6125f-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="6125f-146">Um objeto de sombreador Geometry compilado.</span><span class="sxs-lookup"><span data-stu-id="6125f-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="6125f-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="6125f-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="6125f-148">Membros de [**d3d10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="6125f-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="6125f-149">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="6125f-149">Defining and using state objects</span></span>

<span data-ttu-id="6125f-150">Os objetos de estado são declarados em arquivos FX no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="6125f-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="6125f-151">*StateObjectType* é um dos Estados listados acima e *MemberName* é o nome de qualquer membro que terá um valor não padrão.</span><span class="sxs-lookup"><span data-stu-id="6125f-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="6125f-152">Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false**, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="6125f-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="6125f-153">O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="6125f-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="6125f-154">Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="6125f-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="6125f-155">Para obter um tutorial que descreve o uso de Estados, consulte [Gerenciamento de estado](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6125f-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6125f-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6125f-156">Related topics</span></span>

* [<span data-ttu-id="6125f-157">Sintaxe da técnica de efeito</span><span class="sxs-lookup"><span data-stu-id="6125f-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="6125f-158">Formato de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6125f-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
