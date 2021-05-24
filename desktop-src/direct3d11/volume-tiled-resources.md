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
# <a name="volume-tiled-resources"></a>Alocação dinâmica de volumes de recursos

Texturas de volume (3D) podem ser usadas como recursos lado a lado, notando que a resolução de blocos é tridimensional.

-   [Visão geral](#overview)
-   [APIs de recurso lado a lado D3D11.3](#d3d113-tiled-resource-apis)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Os recursos lado a lado desacodam um objeto de recurso D3D de sua memória de apoio (os recursos no passado tinham uma relação 1:1 com a memória de apoio). Isso permite uma variedade de cenários interessantes, como streaming em dados de textura e reutilação ou redução do uso de memória

Há suporte para recursos lado a lado de textura 2D em D3D11.2. D3D12 e D3D11.3 adicionam suporte para texturas lado a lado 3D.

As dimensões de recursos típicas usadas em peças são 4 x 4 blocos para texturas 2D e 4 x 4 x 4 blocos para texturas 3D.



| Bits/pixel (1 exemplo/pixel)                            | Dimensões deile (pixels, w x h x d)                                    |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |



 

Observe que os seguintes formatos não têm suporte com recursos lado a lado: formatos 96bpp, formatos de vídeo, R1 \_ UNORM, R8G8 \_ B8G8 \_ UNORM, R8R8 \_ G8B8 \_ UNORM.

Nos diagramas abaixo de cinza escuro, representa blocos NULL.

-   [Mapeamento padrão de recurso lado a lado de textura 3D (mip mais detalhado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
-   [Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
-   [Recurso lado a lado 3D de textura (mip mais detalhado)](#texture-3d-tiled-resource-most-detailed-mip)
-   [Recurso lado a lado 3D de textura (segundo mip mais detalhado)](#texture-3d-tiled-resource-second-most-detailed-mip)
-   [Recurso lado a lado 3D de textura (bloco único)](#texture-3d-tiled-resource-single-tile)
-   [Recurso lado a lado 3D de textura (caixa uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mapeamento padrão de recurso lado a lado de textura 3D (mip mais detalhado)

![mapeamento padrão do mip mais detalhado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)

![mapeamento padrão do segundo mip mais detalhado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso lado a lado 3D de textura (mip mais detalhado)

O código a seguir configura um recurso em bloco 3D no mip mais detalhado.

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

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso lado a lado 3D de textura (segundo mip mais detalhado)

O código a seguir configura um recurso em bloco 3D e o segundo mip mais detalhado:

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

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso lado a lado 3D de textura (bloco único)

O código a seguir configura um recurso de único conjunto:

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

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso lado a lado 3D de textura (caixa uniforme)

O código a seguir configura um recurso lado a lado do Uniform Box (observe a instrução `trSize.bUseBox = true;) :`

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

## <a name="d3d113-tiled-resource-apis"></a>APIs de recurso lado a lado D3D11.3

As mesmas chamadas à API são usadas para recursos lado a lado 2D e 3D:

Enumerações

-   [**D3D11 \_ \_ \_ Camada de recursos do lado do xadrez**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) : determina o nível de suporte ao recurso do lado do xadrez.
-   [**D3D11 \_ FORMATO \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) : usado para testar o suporte a recursos lado a lado.
-   [**D3D11 \_ Marque o \_ sinalizador de \_ \_ níveis \_ de qualidade**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag) de vários exemplos: determina o suporte a recursos de um lado em um recurso de várias amostras.
-   [**D3D11 \_ \_ \_ Sinalizadores de cópia de bloco**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag) : mantém os sinalizadores para copiar de e para swizzled de recursos de lado e buffers lineares.

Estruturas

-   [**D3D11 \_ \_ \_ Coordenada de recurso por lado**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate) : contém a referência a co-ordenada x, y e z e o subresource. Observe que há uma classe auxiliar: \_ coordenada de recurso de lado CD3D11 \_ \_ .
-   [**D3D11 \_ \_ \_ Tamanho da região do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size) : especifica o tamanho e o número de blocos da região do lado do ladrilho.
-   [**D3D11 \_ \_Forma do bloco**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape) : a forma do bloco como uma largura, altura e profundidade em texels.
-   [**D3D11 \_ D3D11 de dados de recurso \_ \_ \_ OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1): contém o nível de camada de recurso de bloco com suporte.

Métodos

-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : usado para determinar quais recursos e em que camada têm suporte no hardware atual.
-   [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) : copia blocos do buffer para o recurso de lado ou vice-versa.
-   [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) : atualiza os mapeamentos de locais de bloco em recursos de ladrilho para locais de memória em um pool de blocos.
-   [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) : copia mapeamentos de um recurso de origem ao lado para um recurso de destino ao lado.
-   [**ID3D11DeviceContext2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




