---
title: Recursos de sublado do volume (gráficos do Direct3D 11)
description: Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.
ms.assetid: B6BF22A2-EDA3-4765-B545-BF825043D4C4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb8b35e522ef3298abad1322d6fb7a2fe65bfcf
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103638829"
---
# <a name="volume-tiled-resources"></a><span data-ttu-id="c7d89-103">Alocação dinâmica de volumes de recursos</span><span class="sxs-lookup"><span data-stu-id="c7d89-103">Volume Tiled Resources</span></span>

<span data-ttu-id="c7d89-104">Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.</span><span class="sxs-lookup"><span data-stu-id="c7d89-104">Volume (3D) textures can be used as tiled resources, noting that tile resolution is three-dimensional.</span></span>

-   [<span data-ttu-id="c7d89-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c7d89-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="c7d89-106">APIs de recurso de lado xadrez do D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="c7d89-106">D3D11.3 Tiled Resource APIs</span></span>](#d3d113-tiled-resource-apis)
-   [<span data-ttu-id="c7d89-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7d89-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="c7d89-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="c7d89-108">Overview</span></span>

<span data-ttu-id="c7d89-109">Os recursos ao lado do ladrilho desacoplam um objeto de recurso do D3D de sua memória de backup (os recursos no passado tinham uma relação 1:1 com a memória de backup).</span><span class="sxs-lookup"><span data-stu-id="c7d89-109">Tiled resources decouple a D3D Resource object from its backing memory (resources in the past had a 1:1 relationship with their backing memory).</span></span> <span data-ttu-id="c7d89-110">Isso permite uma variedade de cenários interessantes, como streaming em dados de textura e reutilização ou redução de uso de memória</span><span class="sxs-lookup"><span data-stu-id="c7d89-110">This allows for a variety of interesting scenarios such as streaming in texture data and reusing or reducing memory usage</span></span>

<span data-ttu-id="c7d89-111">os recursos do lado de textura 2D têm suporte no D3D 11.2.</span><span class="sxs-lookup"><span data-stu-id="c7d89-111">2D texture tiled resources are supported in D3D11.2.</span></span> <span data-ttu-id="c7d89-112">D3D12 e D3D 11.3 adicionam suporte para texturas de lado 3D.</span><span class="sxs-lookup"><span data-stu-id="c7d89-112">D3D12 and D3D11.3 add support for 3D tiled textures.</span></span>

<span data-ttu-id="c7d89-113">As dimensões de recurso típicas usadas na disposição de blocos são 4 x 4 blocos para texturas 2D e 4 x 4 x 4 blocos para texturas 3D.</span><span class="sxs-lookup"><span data-stu-id="c7d89-113">The typical resource dimensions used in tiling are 4 x 4 tiles for 2D textures, and 4 x 4 x 4 tiles for 3D textures.</span></span>



|                             |                                     |
|-----------------------------|-------------------------------------|
| <span data-ttu-id="c7d89-114">Bits/pixel (1 amostra/pixel)</span><span class="sxs-lookup"><span data-stu-id="c7d89-114">Bits/pixel (1 sample/pixel)</span></span> | <span data-ttu-id="c7d89-115">Dimensões do bloco (pixels, w x h x d)</span><span class="sxs-lookup"><span data-stu-id="c7d89-115">Tile dimensions (pixels, w x h x d)</span></span> |
| <span data-ttu-id="c7d89-116">8</span><span class="sxs-lookup"><span data-stu-id="c7d89-116">8</span></span>                           | <span data-ttu-id="c7d89-117">64x32x32</span><span class="sxs-lookup"><span data-stu-id="c7d89-117">64x32x32</span></span>                            |
| <span data-ttu-id="c7d89-118">16</span><span class="sxs-lookup"><span data-stu-id="c7d89-118">16</span></span>                          | <span data-ttu-id="c7d89-119">32x32x32</span><span class="sxs-lookup"><span data-stu-id="c7d89-119">32x32x32</span></span>                            |
| <span data-ttu-id="c7d89-120">32</span><span class="sxs-lookup"><span data-stu-id="c7d89-120">32</span></span>                          | <span data-ttu-id="c7d89-121">32x32x16</span><span class="sxs-lookup"><span data-stu-id="c7d89-121">32x32x16</span></span>                            |
| <span data-ttu-id="c7d89-122">64</span><span class="sxs-lookup"><span data-stu-id="c7d89-122">64</span></span>                          | <span data-ttu-id="c7d89-123">32x16x16</span><span class="sxs-lookup"><span data-stu-id="c7d89-123">32x16x16</span></span>                            |
| <span data-ttu-id="c7d89-124">128</span><span class="sxs-lookup"><span data-stu-id="c7d89-124">128</span></span>                         | <span data-ttu-id="c7d89-125">16x16x16</span><span class="sxs-lookup"><span data-stu-id="c7d89-125">16x16x16</span></span>                            |
| <span data-ttu-id="c7d89-126">BC 1, 4</span><span class="sxs-lookup"><span data-stu-id="c7d89-126">BC 1,4</span></span>                      | <span data-ttu-id="c7d89-127">128x64x16</span><span class="sxs-lookup"><span data-stu-id="c7d89-127">128x64x16</span></span>                           |
| <span data-ttu-id="c7d89-128">BC 2, 3, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="c7d89-128">BC 2,3,5,6,7</span></span>                | <span data-ttu-id="c7d89-129">64x64x16</span><span class="sxs-lookup"><span data-stu-id="c7d89-129">64x64x16</span></span>                            |



 

<span data-ttu-id="c7d89-130">Observe que não há suporte para os seguintes formatos com os recursos em ladrilho: formatos 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 G8B8 \_ \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="c7d89-130">Note the following formats are not supported with tiled resources: 96bpp formats, video formats, R1\_UNORM, R8G8\_B8G8\_UNORM, R8R8\_G8B8\_UNORM.</span></span>

<span data-ttu-id="c7d89-131">Nos diagramas abaixo do cinza escuro, representam blocos nulos.</span><span class="sxs-lookup"><span data-stu-id="c7d89-131">In the diagrams below dark gray represents NULL tiles.</span></span>

-   [<span data-ttu-id="c7d89-132">Mapeamento padrão de recurso em ladrilho 3D de textura (MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-132">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [<span data-ttu-id="c7d89-133">Mapeamento padrão de recurso em ladrilho 3D de textura (segundo MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-133">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [<span data-ttu-id="c7d89-134">Recurso de xadrez 3D de textura (MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-134">Texture 3D Tiled Resource (most detailed mip)</span></span>](#texture-3d-tiled-resource-most-detailed-mip)
-   [<span data-ttu-id="c7d89-135">Recurso de xadrez 3D de textura (segundo MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-135">Texture 3D Tiled Resource (second most detailed mip)</span></span>](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [<span data-ttu-id="c7d89-136">Recurso de xadrez 3D de textura (bloco único)</span><span class="sxs-lookup"><span data-stu-id="c7d89-136">Texture 3D Tiled Resource (Single Tile)</span></span>](#texture-3d-tiled-resource-single-tile)
-   [<span data-ttu-id="c7d89-137">Recurso de xadrez 3D de textura (caixa uniforme)</span><span class="sxs-lookup"><span data-stu-id="c7d89-137">Texture 3D Tiled Resource (Uniform Box)</span></span>](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a><span data-ttu-id="c7d89-138">Mapeamento padrão de recurso em ladrilho 3D de textura (MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-138">Texture 3D Tiled Resource default mapping (most detailed mip)</span></span>

![mapeamento padrão do MIP mais detalhado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a><span data-ttu-id="c7d89-140">Mapeamento padrão de recurso em ladrilho 3D de textura (segundo MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-140">Texture 3D Tiled Resource default mapping (second most detailed mip)</span></span>

![mapeamento padrão do segundo MIP mais detalhado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a><span data-ttu-id="c7d89-142">Recurso de xadrez 3D de textura (MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-142">Texture 3D Tiled Resource (most detailed mip)</span></span>

<span data-ttu-id="c7d89-143">O código a seguir configura um recurso de lado 3D no MIP mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="c7d89-143">The following code sets up a 3D tiled resource at the most detailed mip.</span></span>

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

![mapeamento mais detalhado de um recurso de lado 3D](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a><span data-ttu-id="c7d89-145">Recurso de xadrez 3D de textura (segundo MIP mais detalhado)</span><span class="sxs-lookup"><span data-stu-id="c7d89-145">Texture 3D Tiled Resource (second most detailed mip)</span></span>

<span data-ttu-id="c7d89-146">O código a seguir configura um recurso de lado 3D e o segundo MIP mais detalhado:</span><span class="sxs-lookup"><span data-stu-id="c7d89-146">The following code sets up a 3D tiled resource, and the second most detailed mip:</span></span>

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

![segundo mapeamento mais detalhado de um recurso de lado 3D](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a><span data-ttu-id="c7d89-148">Recurso de xadrez 3D de textura (bloco único)</span><span class="sxs-lookup"><span data-stu-id="c7d89-148">Texture 3D Tiled Resource (Single Tile)</span></span>

<span data-ttu-id="c7d89-149">O código a seguir configura um único recurso de bloco:</span><span class="sxs-lookup"><span data-stu-id="c7d89-149">The following code sets up a Single Tile resource:</span></span>

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

![um único bloco](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a><span data-ttu-id="c7d89-151">Recurso de xadrez 3D de textura (caixa uniforme)</span><span class="sxs-lookup"><span data-stu-id="c7d89-151">Texture 3D Tiled Resource (Uniform Box)</span></span>

<span data-ttu-id="c7d89-152">O código a seguir configura um recurso de caixa uniforme em ladrilhos (Observe a instrução `trSize.bUseBox = true;) :`</span><span class="sxs-lookup"><span data-stu-id="c7d89-152">The following code sets up a Uniform Box tiled resource (note the statement `trSize.bUseBox = true;) :`</span></span>

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

## <a name="d3d113-tiled-resource-apis"></a><span data-ttu-id="c7d89-154">APIs de recurso de lado xadrez do D3D 11.3</span><span class="sxs-lookup"><span data-stu-id="c7d89-154">D3D11.3 Tiled Resource APIs</span></span>

<span data-ttu-id="c7d89-155">As mesmas chamadas à API são usadas para recursos de lado 2D e 3D:</span><span class="sxs-lookup"><span data-stu-id="c7d89-155">The same API calls are used for both 2D and 3D tiled resources:</span></span>

<span data-ttu-id="c7d89-156">Enumerações</span><span class="sxs-lookup"><span data-stu-id="c7d89-156">Enums</span></span>

-   <span data-ttu-id="c7d89-157">[**D3D11 \_ \_ \_ Camada de recursos do lado do xadrez**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina o nível de suporte ao recurso do lado do xadrez.</span><span class="sxs-lookup"><span data-stu-id="c7d89-157">[**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determines the level of tiled resource support.</span></span>
-   <span data-ttu-id="c7d89-158">[**D3D11 \_ FORMATO \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : usado para testar o suporte a recursos lado a lado.</span><span class="sxs-lookup"><span data-stu-id="c7d89-158">[**D3D11\_FORMAT\_SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : used to test for tiled resource support.</span></span>
-   <span data-ttu-id="c7d89-159">[**D3D11 \_ Marque o \_ sinalizador de \_ \_ níveis \_ de qualidade**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) de vários exemplos: determina o suporte a recursos de um lado em um recurso de várias amostras.</span><span class="sxs-lookup"><span data-stu-id="c7d89-159">[**D3D11\_CHECK\_MULTISAMPLE\_QUALITY\_LEVELS\_FLAG**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) : determines tiled resource support in a multi-sampling resource.</span></span>
-   <span data-ttu-id="c7d89-160">[**D3D11 \_ \_ \_ Sinalizadores de cópia de bloco**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : mantém os sinalizadores para copiar de e para swizzled de recursos de lado e buffers lineares.</span><span class="sxs-lookup"><span data-stu-id="c7d89-160">[**D3D11\_TILE\_COPY\_FLAGS**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : holds flags for copying to and from swizzled tiled resources and linear buffers.</span></span>

<span data-ttu-id="c7d89-161">Estruturas</span><span class="sxs-lookup"><span data-stu-id="c7d89-161">Structures</span></span>

-   <span data-ttu-id="c7d89-162">[**D3D11 \_ \_ \_ Coordenada de recurso por lado**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contém a referência a co-ordenada x, y e z e o subresource.</span><span class="sxs-lookup"><span data-stu-id="c7d89-162">[**D3D11\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : holds the x, y, and z co-ordinate, and subresource reference.</span></span> <span data-ttu-id="c7d89-163">Observe que há uma classe auxiliar: \_ coordenada de recurso de lado CD3D11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c7d89-163">Note there is a helper class: CD3D11\_TILED\_RESOURCE\_COORDINATE.</span></span>
-   <span data-ttu-id="c7d89-164">[**D3D11 \_ \_ \_ Tamanho da região do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : especifica o tamanho e o número de blocos da região do lado do ladrilho.</span><span class="sxs-lookup"><span data-stu-id="c7d89-164">[**D3D11\_TILE\_REGION\_SIZE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : specifies the size, and number of tiles, of the tiled region.</span></span>
-   <span data-ttu-id="c7d89-165">[**D3D11 \_ \_Forma do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : a forma do bloco como uma largura, altura e profundidade em texels.</span><span class="sxs-lookup"><span data-stu-id="c7d89-165">[**D3D11\_TILE\_SHAPE**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : the tile shape as a width, height and depth in texels.</span></span>
-   <span data-ttu-id="c7d89-166">[**D3D11 \_ D3D11 de dados de recurso \_ \_ \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contém o nível de camada de recurso de bloco com suporte.</span><span class="sxs-lookup"><span data-stu-id="c7d89-166">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): holds the supported tile resource tier level.</span></span>

<span data-ttu-id="c7d89-167">Métodos</span><span class="sxs-lookup"><span data-stu-id="c7d89-167">Methods</span></span>

-   <span data-ttu-id="c7d89-168">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : usado para determinar quais recursos e em que camada têm suporte no hardware atual.</span><span class="sxs-lookup"><span data-stu-id="c7d89-168">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : used to determine what features, and at what tier, are supported by the current hardware.</span></span>
-   <span data-ttu-id="c7d89-169">[**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia blocos do buffer para o recurso de lado ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c7d89-169">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copies tiles from buffer to tiled resource or vice versa.</span></span>
-   <span data-ttu-id="c7d89-170">[**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : atualiza os mapeamentos de locais de bloco em recursos de ladrilho para locais de memória em um pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="c7d89-170">[**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : updates mappings of tile locations in tiled resources to memory locations in a tile pool.</span></span>
-   <span data-ttu-id="c7d89-171">[**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia mapeamentos de um recurso de origem ao lado para um recurso de destino ao lado.</span><span class="sxs-lookup"><span data-stu-id="c7d89-171">[**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copies mappings from a source tiled resource to a destination tiled resource.</span></span>
-   <span data-ttu-id="c7d89-172">[**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.</span><span class="sxs-lookup"><span data-stu-id="c7d89-172">[**ID3D11DeviceContext2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : gets info about how a tiled resource is broken into tiles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7d89-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7d89-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7d89-174">Recursos do Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="c7d89-174">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> </dl>

 

 




