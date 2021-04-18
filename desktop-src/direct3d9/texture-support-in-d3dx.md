---
description: D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Suporte a textura em D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764437"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="a7ee4-104">Suporte a textura em D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a7ee4-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="a7ee4-105">D3DX é uma biblioteca de utilitários que fornece serviços auxiliares.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="a7ee4-106">É uma camada acima do componente do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="a7ee4-107">Texturas</span><span class="sxs-lookup"><span data-stu-id="a7ee4-107">Textures</span></span>

<span data-ttu-id="a7ee4-108">Há suporte para várias texturas diferentes nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="a7ee4-109">Suporte a textura padrão do mipmapped.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="a7ee4-110">Consulte [geração automática de mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="a7ee4-111">Suporte ao mapa do cubo.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-111">Cube map support.</span></span> <span data-ttu-id="a7ee4-112">Consulte [mapeamento de ambiente cúbico (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="a7ee4-113">Suporte a textura de volume.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-113">Volume texture support.</span></span> <span data-ttu-id="a7ee4-114">Consulte [recursos de textura de volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="a7ee4-115">Suporte a mapeamento de ambiente.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-115">Environment mapping support.</span></span> <span data-ttu-id="a7ee4-116">Consulte [mapeamento de ambiente (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="a7ee4-117">Suporte ao mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-117">Bump mapping support.</span></span> <span data-ttu-id="a7ee4-118">Consulte [mapeamento de relevo (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="a7ee4-119">Conversão de cores de textura</span><span class="sxs-lookup"><span data-stu-id="a7ee4-119">Texture Color Conversion</span></span>

<span data-ttu-id="a7ee4-120">Ao usar qualquer uma das funções D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx ou D3DXCreateVolumeTexturexxx, talvez seja necessário executar a conversão de cores.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="a7ee4-121">Por exemplo, uma superfície pode ser do tipo RGBA e a outra pode ser UVWQ.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="a7ee4-122">Para casos de formatos diferentes, a sequência de conversão é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="a7ee4-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="a7ee4-123">Mapeando RGBA para UVWQ</span><span class="sxs-lookup"><span data-stu-id="a7ee4-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="a7ee4-124">R <-> U, o canal R é mapeado para o canal U ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-125">G <-> V, G Channel é mapeado para o canal V ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-126">B <-> W, o canal B é mapeado para o canal W ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-127">R <-> Q/L, um canal é mapeado para o canal Q ou L (dependendo de qual está disponível no formato de destino) ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="a7ee4-128">Mapeamento de UV para RGBA</span><span class="sxs-lookup"><span data-stu-id="a7ee4-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="a7ee4-129">U <-> R, o canal U é mapeado para o canal R ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-130">V <-> G, V Channel é mapeado para o canal G, ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-131">1 <-> B, 1 é mapeado para o canal B ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="a7ee4-132">1 <-> A, 1 é mapeado para um canal, ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="a7ee4-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="a7ee4-133">Se um canal não existir na origem, será considerado 1 (com exceção de A8, em que R, G, B será considerado 0).</span><span class="sxs-lookup"><span data-stu-id="a7ee4-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="a7ee4-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a7ee4-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="a7ee4-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7ee4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7ee4-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="a7ee4-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



