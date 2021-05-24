---
title: Recursos lado a lado de volume (elementos gráficos direct3D 11)
description: Saiba como as texturas de volume (3D) podem ser usadas como recursos lado a lado. Observe que a resolução deiles é tridimensional.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf9b3ed8b1db89d9718fa904eefd23ce2e871db
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335430"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="71ab5-104">Alocação dinâmica de volumes de recursos</span><span class="sxs-lookup"><span data-stu-id="71ab5-104">Volume Tiled Resources</span></span>

<span data-ttu-id="71ab5-105">Texturas de volume (3D) podem ser usadas como recursos lado a lado, notando que a resolução de blocos é tridimensional.</span><span class="sxs-lookup"><span data-stu-id="71ab5-105">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="71ab5-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="71ab5-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="71ab5-107">APIs de recurso lado a lado D3D11.3</span><span class="sxs-lookup"><span data-stu-id="71ab5-107">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="71ab5-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71ab5-108">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="71ab5-109">Visão geral</span><span class="sxs-lookup"><span data-stu-id="71ab5-109">Overview</span></span>

<span data-ttu-id="71ab5-110">Os recursos lado a lado desacodam um objeto de recurso D3D de sua memória de apoio (os recursos no passado tinham uma relação 1:1 com a memória de apoio).</span><span class="sxs-lookup"><span data-stu-id="71ab5-110">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="71ab5-111">Isso permite uma variedade de cenários interessantes, como streaming em dados de textura e reutilação ou redução do uso de memória</span><span class="sxs-lookup"><span data-stu-id="71ab5-111">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="71ab5-112">Há suporte para recursos lado a lado de textura 2D em D3D11.2.</span><span class="sxs-lookup"><span data-stu-id="71ab5-112">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="71ab5-113">D3D12 e D3D11.3 adicionam suporte para texturas lado a lado 3D.</span><span class="sxs-lookup"><span data-stu-id="71ab5-113">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="71ab5-114">As dimensões de recursos típicas usadas em peças são 4 x 4 blocos para texturas 2D e 4 x 4 x 4 blocos para texturas 3D.</span><span class="sxs-lookup"><span data-stu-id="71ab5-114">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



| <span data-ttu-id="71ab5-115">Bits/pixel (1 exemplo/pixel)</span><span class="sxs-lookup"><span data-stu-id="71ab5-115">Bits/pixel (1 sample/pixel)</span></span>                            | <span data-ttu-id="71ab5-116">Dimensões deile (pixels, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="71ab5-116">Tile dimensions (pixels, w x h x d)</span></span>                                    |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="71ab5-117">8</span><span class="sxs-lookup"><span data-stu-id="71ab5-117">8</span></span>                           | <span data-ttu-id="71ab5-118">64x32x32</span><span class="sxs-lookup"><span data-stu-id="71ab5-118">64x32x32</span></span>                            |
| <span data-ttu-id="71ab5-119">16</span><span class="sxs-lookup"><span data-stu-id="71ab5-119">16</span></span>                          | <span data-ttu-id="71ab5-120">32x32x32</span><span class="sxs-lookup"><span data-stu-id="71ab5-120">32x32x32</span></span>                            |
| <span data-ttu-id="71ab5-121">32</span><span class="sxs-lookup"><span data-stu-id="71ab5-121">32</span></span>                          | <span data-ttu-id="71ab5-122">32x32x16</span><span class="sxs-lookup"><span data-stu-id="71ab5-122">32x32x16</span></span>                            |
| <span data-ttu-id="71ab5-123">64</span><span class="sxs-lookup"><span data-stu-id="71ab5-123">64</span></span>                          | <span data-ttu-id="71ab5-124">32x16x16</span><span class="sxs-lookup"><span data-stu-id="71ab5-124">32x16x16</span></span>                            |
| <span data-ttu-id="71ab5-125">128</span><span class="sxs-lookup"><span data-stu-id="71ab5-125">128</span></span>                         | <span data-ttu-id="71ab5-126">16x16x16</span><span class="sxs-lookup"><span data-stu-id="71ab5-126">16x16x16</span></span>                            |
| <span data-ttu-id="71ab5-127">BC 1,4</span><span class="sxs-lookup"><span data-stu-id="71ab5-127">BC 1,4</span></span>                      | <span data-ttu-id="71ab5-128">128x64x16</span><span class="sxs-lookup"><span data-stu-id="71ab5-128">128x64x16</span></span>                           |
| <span data-ttu-id="71ab5-129">BC 2,3,5,6,7</span><span class="sxs-lookup"><span data-stu-id="71ab5-129">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="71ab5-130">64x64x16</span><span class="sxs-lookup"><span data-stu-id="71ab5-130">64x64x16</span></span>                            |



 

<span data-ttu-id="71ab5-131">Observe que os seguintes formatos não têm suporte com recursos lado a lado: formatos 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="71ab5-131">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="71ab5-132">Nos diagramas abaixo de cinza escuro, representa blocos NULL.</span><span class="sxs-lookup"><span data-stu-id="71ab5-132">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="71ab5-133">Mapeamento padrão de recurso lado a lado de textura 3D (mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-133">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="71ab5-134">Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-134">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="71ab5-135">Recurso lado a lado 3D de textura (mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-135">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="71ab5-136">Recurso lado a lado 3D de textura (segundo mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-136">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="71ab5-137">Recurso lado a lado 3D de textura (bloco único)</span><span class="sxs-lookup"><span data-stu-id="71ab5-137">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="71ab5-138">Recurso lado a lado 3D de textura (caixa uniforme)</span><span class="sxs-lookup"><span data-stu-id="71ab5-138">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="71ab5-139">Mapeamento padrão de recurso lado a lado de textura 3D (mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-139">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mapeamento padrão do mip mais detalhado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="71ab5-141">Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-141">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![mapeamento padrão do segundo mip mais detalhado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="71ab5-143">Recurso lado a lado 3D de textura (mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-143">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="71ab5-144">O código a seguir configura um recurso em bloco 3D no mip mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="71ab5-144">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![mapeamento mais detalhado de um recurso lado a lado 3d](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="71ab5-146">Recurso lado a lado 3D de textura (segundo mip mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="71ab5-146">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="71ab5-147">O código a seguir configura um recurso em bloco 3D e o segundo mip mais detalhado:</span><span class="sxs-lookup"><span data-stu-id="71ab5-147">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![segundo mapeamento mais detalhado de um recurso lado a lado 3d](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="71ab5-149">Recurso lado a lado 3D de textura (bloco único)</span><span class="sxs-lookup"><span data-stu-id="71ab5-149">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="71ab5-150">O código a seguir configura um recurso de único conjunto:</span><span class="sxs-lookup"><span data-stu-id="71ab5-150">The following code sets up a Single Tile resource:</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![um único único só](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="71ab5-152">Recurso lado a lado 3D de textura (caixa uniforme)</span><span class="sxs-lookup"><span data-stu-id="71ab5-152">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="71ab5-153">O código a seguir configura um recurso lado a lado do Uniform Box (observe a instrução `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="71ab5-153">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

``` syntax
D3D11_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D11_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![uma caixa uniforme](images/vtr-tex3d-uniform.png)

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="71ab5-155">APIs de recurso lado a lado D3D11.3</span><span class="sxs-lookup"><span data-stu-id="71ab5-155">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="71ab5-156">As mesmas chamadas à API são usadas para recursos lado a lado 2D e 3D:</span><span class="sxs-lookup"><span data-stu-id="71ab5-156">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="71ab5-157">Enumerações</span><span class="sxs-lookup"><span data-stu-id="71ab5-157">Enums</span></span>

-   <span data-ttu-id="71ab5-158">[**D3D11 \_ \_ \_ Camada de recursos do lado do xadrez**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina o nível de suporte ao recurso do lado do xadrez.</span><span class="sxs-lookup"><span data-stu-id="71ab5-158">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="71ab5-159">[**D3D11 \_ FORMATO \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : usado para testar o suporte a recursos lado a lado.</span><span class="sxs-lookup"><span data-stu-id="71ab5-159">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="71ab5-160">[**D3D11 \_ Marque o \_ sinalizador de \_ \_ níveis \_ de qualidade**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) de vários exemplos: determina o suporte a recursos de um lado em um recurso de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="71ab5-160">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="71ab5-161">[**D3D11 \_ \_ \_ Sinalizadores de cópia de bloco**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : mantém os sinalizadores para copiar de e para swizzled de recursos de lado e buffers lineares.</span><span class="sxs-lookup"><span data-stu-id="71ab5-161">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="71ab5-162">Estruturas</span><span class="sxs-lookup"><span data-stu-id="71ab5-162">Structures</span></span>

-   <span data-ttu-id="71ab5-163">[**D3D11 \_ \_ \_ Coordenada de recurso por lado**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contém a referência a co-ordenada x, y e z e o subresource.</span><span class="sxs-lookup"><span data-stu-id="71ab5-163">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="71ab5-164">Observe que há uma classe auxiliar: \_ coordenada de recurso de lado CD3D11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="71ab5-164">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="71ab5-165">[**D3D11 \_ \_ \_ Tamanho da região do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : especifica o tamanho e o número de blocos da região do lado do ladrilho.</span><span class="sxs-lookup"><span data-stu-id="71ab5-165">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="71ab5-166">[**D3D11 \_ \_Forma do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : a forma do bloco como uma largura, altura e profundidade em texels.</span><span class="sxs-lookup"><span data-stu-id="71ab5-166">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="71ab5-167">[**D3D11 \_ D3D11 de dados de recurso \_ \_ \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contém o nível de camada de recurso de bloco com suporte.</span><span class="sxs-lookup"><span data-stu-id="71ab5-167">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="71ab5-168">Métodos</span><span class="sxs-lookup"><span data-stu-id="71ab5-168">Methods</span></span>

-   <span data-ttu-id="71ab5-169">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : usado para determinar quais recursos e em que camada têm suporte no hardware atual.</span><span class="sxs-lookup"><span data-stu-id="71ab5-169">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="71ab5-170">[**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia blocos do buffer para o recurso de lado ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="71ab5-170">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="71ab5-171">[**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : atualiza os mapeamentos de locais de bloco em recursos de ladrilho para locais de memória em um pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="71ab5-171">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="71ab5-172">[**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia mapeamentos de um recurso de origem ao lado para um recurso de destino ao lado.</span><span class="sxs-lookup"><span data-stu-id="71ab5-172">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="71ab5-173">[**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.</span><span class="sxs-lookup"><span data-stu-id="71ab5-173">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71ab5-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71ab5-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ab5-175">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="71ab5-175">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




