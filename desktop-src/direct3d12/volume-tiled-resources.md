---
title: Recursos de sublado do volume (Direct3D 12)
description: Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8d6e9b4d7ae9ad4b93bae5cf29749c293bf7f55ea7fa35a1e1ca71040218e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123484"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Recursos de sublado do volume (Direct3D 12)

Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.

## <a name="overview"></a>Visão geral

Os recursos ao lado do xadrez desacoplam um objeto de recurso do Direct3D de sua memória de backup (os recursos no passado tinham uma relação 1:1 com a memória de backup). Isso permite uma variedade de cenários interessantes, como streaming em dados de textura e reutilização ou redução de uso de memória.

os recursos do lado de textura 2D têm suporte no Direct3D 11,2. O suporte opcional para texturas de lado 3D está disponível para o Direct3D 12 e o Direct3D 11,3 (consulte [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

As dimensões de recurso típicas usadas na disposição de blocos são 4 x 4 blocos para texturas 2D e 4 x 4 x 4 blocos para texturas 3D.

| Bits/pixel (1 amostra/pixel) | Dimensões do bloco (pixels, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1, 4                      | 128x64x16                           |
| BC 2, 3, 5, 6, 7                | 64x64x16                            |

Observe que não há suporte para os seguintes formatos com os recursos em ladrilho: formatos de 96bpp, formatos de vídeo, **R1_UNORM**, **R8G8_B8G8_UNORM** **R8R8_G8B8_UNORM**.

Nos diagramas abaixo, cinza escuro representa blocos nulos.

* [Mapeamento padrão de recurso em ladrilho 3D de textura (MIP mais detalhado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Mapeamento padrão de recurso em ladrilho 3D de textura (segundo MIP mais detalhado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Recurso de xadrez 3D de textura (MIP mais detalhado)](#texture-3d-tiled-resource-most-detailed-mip)
* [Recurso de xadrez 3D de textura (segundo MIP mais detalhado)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Recurso de xadrez 3D de textura (bloco único)](#texture-3d-tiled-resource-single-tile)
* [Recurso de xadrez 3D de textura (caixa uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mapeamento padrão de recurso em ladrilho 3D de textura (MIP mais detalhado)

![mapeamento padrão de um recurso tridimensional em ladrilhos](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mapeamento padrão de recurso em ladrilho 3D de textura (segundo mais detalhado, MIP)

![mostra a segunda parte mais detalhada do MIP](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso de lado 3D de textura (MIP mais detalhado)

O código a seguir configura um recurso de lado 3D no MIP mais detalhado.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord{};
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize{};
trSize.bUseBox = false;
trSize.NumTiles = 63;
```

![MIP mais detalhado para uma textura tridimensional](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso de xadrez 3D de textura (mais de um MIP detalhado)

O código a seguir configura um recurso de lado 3D e o segundo MIP mais detalhado.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 0;
trCoord.Z = 0;
trCoord.Subresource = 1;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = false;
trSize.NumTiles = 6;
```

![um segundo mais detalhado de MIP para uma textura tridimensional](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso de xadrez 3D de textura (bloco único)

O código a seguir configura um único recurso de bloco.

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 1;
trCoord.Y = 1;
trCoord.Z = 1;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![um recurso de três dimensões de lado único](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso de xadrez 3D de textura (caixa uniforme)

O código a seguir configura um recurso de caixa uniforme em ladrilhos (Observe a instrução `trSize.bUseBox = true;) :`

```cpp
D3D12_TILED_RESOURCE_COORDINATE trCoord;
trCoord.X = 0;
trCoord.Y = 1;
trCoord.Z = 0;
trCoord.Subresource = 0;

D3D12_TILE_REGION_SIZE trSize;
trSize.bUseBox = true;
trSize.NumTiles = 27;
trSize.Width = 3;
trSize.Height = 3;
trSize.Depth = 3;
```

![uma caixa uniforme](images/vtr-tex3d-uniform.png)

## <a name="tiled-resource-apis"></a>APIs de recursos de lado

As mesmas chamadas à API são usadas para recursos de lado 2D e 3D.

Enumerações

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina o nível de suporte ao recurso de lado do xadrez.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : usado para testar o suporte a recursos de lado do xadrez.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina o suporte a recursos em vários ladrilhos em um recurso de várias amostras.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : mantém os sinalizadores para copiar de e para swizzled de recursos de lado e buffers lineares.

Estruturas

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contém a referência de subrecurso x, y e z e o subresource. Observe que há uma estrutura auxiliar: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : especifica o tamanho e o número de blocos da região do lado do xadrez.
* [**D3D12_TILE_SHAPE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) : a forma do bloco como uma largura, altura e profundidade em texels.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : mantém o nível de camada de recurso de bloco com suporte e um booliano, *VolumeTiledResourcesSupported*, indicados se há suporte para os recursos de sublado de volume.

Métodos

* [**ID3D12Device:: CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : usado para determinar quais recursos e em que camada têm suporte no hardware atual.
* [**ID3D12GraphicsCommandList:: CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) : copia blocos do buffer para o recurso de lado ou vice-versa.
* [**ID3D12CommandQueue:: UpdateTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) : atualiza os mapeamentos de locais de bloco em recursos de blocos gráficos para locais de memória em um heap de recursos.
* [**ID3D12CommandQueue:: CopyTileMappings**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) : copia mapeamentos de um recurso de origem ao lado para um recurso de destino ao lado.
* [**ID3D12Device:: GetResourceTiling**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) : Obtém informações sobre como um recurso de quebra-lado é dividido em blocos.

## <a name="related-topics"></a>Tópicos relacionados

* [Associação de recursos](resource-binding.md)
