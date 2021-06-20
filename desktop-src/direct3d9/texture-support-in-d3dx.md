---
description: Saiba mais sobre o suporte à textura no D3DX. D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Suporte à textura no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404599"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="350cb-105">Suporte à textura no D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="350cb-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="350cb-106">D3DX é uma biblioteca de utilitários que fornece serviços auxiliares.</span><span class="sxs-lookup"><span data-stu-id="350cb-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="350cb-107">É uma camada acima do componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="350cb-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="350cb-108">Texturas</span><span class="sxs-lookup"><span data-stu-id="350cb-108">Textures</span></span>

<span data-ttu-id="350cb-109">Há suporte para muitas texturas diferentes nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="350cb-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="350cb-110">Suporte à textura mapeada padrão.</span><span class="sxs-lookup"><span data-stu-id="350cb-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="350cb-111">Consulte [Geração automática de Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="350cb-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="350cb-112">Suporte ao mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="350cb-112">Cube map support.</span></span> <span data-ttu-id="350cb-113">Consulte [Mapeamento de ambiente cúbica (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="350cb-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="350cb-114">Suporte à textura de volume.</span><span class="sxs-lookup"><span data-stu-id="350cb-114">Volume texture support.</span></span> <span data-ttu-id="350cb-115">Consulte [Recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="350cb-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="350cb-116">Suporte ao mapeamento de ambiente.</span><span class="sxs-lookup"><span data-stu-id="350cb-116">Environment mapping support.</span></span> <span data-ttu-id="350cb-117">Consulte [Mapeamento de ambiente (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="350cb-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="350cb-118">Suporte ao mapeamento de aumento.</span><span class="sxs-lookup"><span data-stu-id="350cb-118">Bump mapping support.</span></span> <span data-ttu-id="350cb-119">Consulte [Mapeamento de aumento (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="350cb-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="350cb-120">Conversão de cor de textura</span><span class="sxs-lookup"><span data-stu-id="350cb-120">Texture Color Conversion</span></span>

<span data-ttu-id="350cb-121">Ao usar qualquer uma das funções D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, a conversão de cores pode precisar ser executada.</span><span class="sxs-lookup"><span data-stu-id="350cb-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="350cb-122">Por exemplo, uma superfície pode ser do tipo RGBA e a outra pode ser UVWQ.</span><span class="sxs-lookup"><span data-stu-id="350cb-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="350cb-123">Para casos de formatos diferentes, a sequência de conversão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="350cb-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="350cb-124">Mapeando RGBA para UVWQ</span><span class="sxs-lookup"><span data-stu-id="350cb-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="350cb-125">R <-> U, o canal R é mapeado para o canal U ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-126">G <-> V, o canal G é mapeado para o canal V ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-127">B <-> W, o canal B é mapeado para o canal W ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-128">Um <-> P/L, um canal é mapeado para o canal Q ou L (dependendo de qual está disponível no formato de destino) ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="350cb-129">Mapeando UV para RGBA</span><span class="sxs-lookup"><span data-stu-id="350cb-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="350cb-130">U <-> R, o canal U é mapeado para o canal R ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-131">V <-> G, o canal V é mapeado para o canal G ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-132">1 <-> B, 1 é mapeado para o canal B ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="350cb-133">1 <-> A, 1 é mapeado para o canal A ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="350cb-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="350cb-134">Se um canal não existir na origem, supõe-se que seja 1 (com exceção de A8, em que R,G,B é presumido como 0).</span><span class="sxs-lookup"><span data-stu-id="350cb-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="350cb-135">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="350cb-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="350cb-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="350cb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="350cb-137">D3dx</span><span class="sxs-lookup"><span data-stu-id="350cb-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



