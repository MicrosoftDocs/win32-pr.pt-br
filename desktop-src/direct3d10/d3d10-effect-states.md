---
description: Os Estados de efeito são pares de nome-valor na forma de uma expressão.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104297997"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="5dee4-103">Grupos de estado de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5dee4-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="5dee4-104">Os Estados de efeito são pares de nome-valor na forma de uma expressão.</span><span class="sxs-lookup"><span data-stu-id="5dee4-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="5dee4-105">Estado do Blend</span><span class="sxs-lookup"><span data-stu-id="5dee4-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="5dee4-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="5dee4-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="5dee4-107">Membros de [ **d3d10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="5dee4-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="5dee4-108">Profundidade e estado do estêncil</span><span class="sxs-lookup"><span data-stu-id="5dee4-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="5dee4-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="5dee4-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="5dee4-110">Membros do [ **\_ estêncil de profundidade d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="5dee4-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="5dee4-111">FRONTFACESTENCILFAIL \* \*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="5dee4-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="5dee4-112">Membro de [ **d3d10 \_ profundidade \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="5dee4-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="5dee4-113">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="5dee4-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="5dee4-114">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="5dee4-114">FILLMODE</span></span> | [<span data-ttu-id="5dee4-115">**\_Modo de preenchimento d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="5dee4-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="5dee4-116">De seleção</span><span class="sxs-lookup"><span data-stu-id="5dee4-116">CULLMODE</span></span> | [<span data-ttu-id="5dee4-117">**\_Modo de seleção de d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="5dee4-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="5dee4-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="5dee4-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="5dee4-119">Membros do [ **\_ rasterizador d3d10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="5dee4-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="5dee4-120">Estado de amostra</span><span class="sxs-lookup"><span data-stu-id="5dee4-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="5dee4-121">**Filtro**, **endereçou**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="5dee4-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="5dee4-122">Membros de [ **amostra de d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="5dee4-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="5dee4-123">Consulte [tipo de amostra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obter exemplos.</span><span class="sxs-lookup"><span data-stu-id="5dee4-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="5dee4-124">Estado do objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="5dee4-124">Effect object state</span></span>

| <span data-ttu-id="5dee4-125">Este objeto de efeito</span><span class="sxs-lookup"><span data-stu-id="5dee4-125">This effect object</span></span> | <span data-ttu-id="5dee4-126">É mapeada para</span><span class="sxs-lookup"><span data-stu-id="5dee4-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="5dee4-127">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="5dee4-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="5dee4-128">Um objeto de estado de [estado do rasterizador](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="5dee4-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="5dee4-129">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="5dee4-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="5dee4-130">Um objeto de estado de [estado de profundidade e de estêncil](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="5dee4-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="5dee4-131">BLENDstate</span><span class="sxs-lookup"><span data-stu-id="5dee4-131">BLENDSTATE</span></span> | <span data-ttu-id="5dee4-132">Um objeto de estado de [estado de mistura](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="5dee4-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="5dee4-133">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="5dee4-133">VERTEXSHADER</span></span> | <span data-ttu-id="5dee4-134">Um objeto de sombreador de vértice compilado.</span><span class="sxs-lookup"><span data-stu-id="5dee4-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="5dee4-135">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="5dee4-135">PIXELSHADER</span></span> | <span data-ttu-id="5dee4-136">Um objeto de sombreador de pixel compilado.</span><span class="sxs-lookup"><span data-stu-id="5dee4-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="5dee4-137">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="5dee4-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="5dee4-138">Um objeto de sombreador Geometry compilado.</span><span class="sxs-lookup"><span data-stu-id="5dee4-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="5dee4-139">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="5dee4-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="5dee4-140">Membros de [**d3d10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="5dee4-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="5dee4-141">Definindo e usando objetos de estado</span><span class="sxs-lookup"><span data-stu-id="5dee4-141">Defining and using state objects</span></span>

<span data-ttu-id="5dee4-142">Os objetos de estado são declarados em arquivos FX no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="5dee4-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="5dee4-143">*StateObjectType* é um dos Estados listados acima e *MemberName* é o nome de qualquer membro que terá um valor não padrão.</span><span class="sxs-lookup"><span data-stu-id="5dee4-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="5dee4-144">Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false**, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="5dee4-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="5dee4-145">O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5dee4-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="5dee4-146">Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.</span><span class="sxs-lookup"><span data-stu-id="5dee4-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="5dee4-147">Para obter um tutorial que descreve o uso de Estados, consulte [Gerenciamento de estado](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="5dee4-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dee4-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dee4-148">Related topics</span></span>

* [<span data-ttu-id="5dee4-149">Sintaxe da técnica de efeito</span><span class="sxs-lookup"><span data-stu-id="5dee4-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="5dee4-150">Formato de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5dee4-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
