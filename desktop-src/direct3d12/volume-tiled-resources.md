---
title: Recursos lado a lado do volume (Direct3D 12)
description: Texturas de volume (3D) podem ser usadas como recursos lado a lado, notando que a resolução de blocos é tridimensional.
ms.assetid: F670D15D-BC0F-4F90-99C1-A35192FE8980
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5371926b38415a84803155c67ea70ed902b915
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436301"
---
# <a name="volume-tiled-resources-direct3d-12"></a>Recursos lado a lado do volume (Direct3D 12)

Texturas de volume (3D) podem ser usadas como recursos lado a lado, notando que a resolução de blocos é tridimensional.

## <a name="overview"></a>Visão geral

Os recursos lado a lado desacodam um objeto de recurso Direct3D de sua memória de apoio (os recursos no passado tinham uma relação 1:1 com a memória de apoio). Isso permite uma variedade de cenários interessantes, como streaming em dados de textura e reutilação ou redução do uso de memória.

Há suporte para recursos lado a lado de textura 2D no Direct3D 11.2. O suporte opcional para texturas lado a lado 3D está disponível para Direct3D 12 e Direct3D 11.3 (consulte [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)).

As dimensões de recursos típicas usadas em peças são 4 x 4 blocos para texturas 2D e 4 x 4 x 4 blocos para texturas 3D.

| Bits/pixel (1 exemplo/pixel) | Dimensões deile (pixels, w x h x d) |
|-----------------------------|-------------------------------------|
| 8                           | 64x32x32                            |
| 16                          | 32x32x32                            |
| 32                          | 32x32x16                            |
| 64                          | 32x16x16                            |
| 128                         | 16x16x16                            |
| BC 1,4                      | 128x64x16                           |
| BC 2,3,5,6,7                | 64x64x16                            |

Observe que não há suporte para os seguintes formatos com recursos lado a lado: formatos de 96bpp, formatos de vídeo, **R1_UNORM**, **R8G8_B8G8_UNORM**, **R8R8_G8B8_UNORM**.

Nos diagramas abaixo, cinza escuro representa blocos NULL.

* [Mapeamento padrão de recurso lado a lado de textura 3D (mip mais detalhado)](#texture-3d-tiled-resource-default-mapping-most-detailed-mip)
* [Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)](#texture-3d-tiled-resource-default-mapping-second-most-detailed-mip)
* [Recurso lado a lado 3D de textura (mip mais detalhado)](#texture-3d-tiled-resource-most-detailed-mip)
* [Recurso lado a lado 3D de textura (segundo mip mais detalhado)](#texture-3d-tiled-resource-second-most-detailed-mip)
* [Recurso lado a lado 3D de textura (bloco único)](#texture-3d-tiled-resource-single-tile)
* [Recurso lado a lado 3D de textura (caixa uniforme)](#texture-3d-tiled-resource-uniform-box)

### <a name="texture-3d-tiled-resource-default-mapping-most-detailed-mip"></a>Mapeamento padrão de recurso lado a lado da textura 3D (mip mais detalhado)

![mapeamento padrão de um recurso tridimensional lado a lado](images/vtr-tex3d-default-1.png)

### <a name="texture-3d-tiled-resource-default-mapping-second-most-detailed-mip"></a>Mapeamento padrão de recurso lado a lado de textura 3D (segundo mip mais detalhado)

![mostra o segundo mip mais detalhado](images/vtr-tex3d-default-2.png)

### <a name="texture-3d-tiled-resource-most-detailed-mip"></a>Recurso lado a lado de textura 3D (mip mais detalhado)

O código a seguir configura um recurso em bloco 3D no mip mais detalhado.

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

![mip mais detalhado para uma textura tridimensional](images/vtr-tex3d-default-1b.png)

### <a name="texture-3d-tiled-resource-second-most-detailed-mip"></a>Recurso lado a lado de textura 3D (segundo mip mais detalhado)

O código a seguir configura um recurso em bloco 3D e o segundo mip mais detalhado.

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

![segunda mip mais detalhada para uma textura tridimensional](images/vtr-tex3d-default-2b.png)

### <a name="texture-3d-tiled-resource-single-tile"></a>Recurso lado a lado 3D de textura (bloco único)

O código a seguir configura um único recurso deile.

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

![um recurso tridimensional de bloco único](images/vtr-tex3d-single.png)

### <a name="texture-3d-tiled-resource-uniform-box"></a>Recurso lado a lado 3D de textura (caixa uniforme)

O código a seguir configura um recurso uniforme lado a lado (observe a instrução `trSize.bUseBox = true;) :`

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

## <a name="tiled-resource-apis"></a>APIs de recurso lado a lado

As mesmas chamadas à API são usadas para recursos em bloco 2D e 3D.

Enumerações

* [**D3D12_TILED_RESOURCES_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier) : determina o nível de suporte a recursos lado a lado.
* [**D3D12_FORMAT_SUPPORT2**](/windows/win32/api/d3d12/ne-d3d12-d3d12_format_support2) : usado para testar o suporte a recursos lado a lado.
* [**D3D12_MULTISAMPLE_QUALITY_LEVEL_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_multisample_quality_level_flags) : determina o suporte a recursos lado a lado em um recurso de várias amostragem.
* [**D3D12_TILE_COPY_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_tile_copy_flags) : contém sinalizadores para copiar de e para recursos em blocos swizzled e buffers lineares.

Estruturas

* [**D3D12_TILED_RESOURCE_COORDINATE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) : contém a referência de coordenadas x, y e z e sub-recursos. Observe que há uma estrutura auxiliar: [**CD3DX12_TILED_RESOURCE_COORDINATE**](cd3dx12-tiled-resource-coordinate.md).
* [**D3D12_TILE_REGION_SIZE**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_region_size) : especifica o tamanho e o número de blocos da região lado a lado.
* [**D3D12_TILE_SHAPE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_tile_shape) a forma do seu tamanho como largura, altura e profundidade em texels.
* [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : contém o nível da camada de recurso do bloco com suporte e um boolianos, *VolumeTiledResourcesSupported*, indicaram se há suporte para recursos com bloco de volume.

Métodos

* [**ID3D12Device::CheckFeatureSupport:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) usado para determinar quais recursos e em qual camada têm suporte no hardware atual.
* [**ID3D12GraphicsCommandList::CopyTiles:**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles) copia blocos do buffer para o recurso lado a lado ou vice-versa.
* [**ID3D12CommandQueue::UpdateTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) atualiza mapeamentos de locais de bloco em recursos lado a lado para locais de memória em um heap de recursos.
* [**ID3D12CommandQueue::CopyTileMappings:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings) copia mapeamentos de um recurso de origem lado a lado para um recurso lado a lado de destino.
* [**ID3D12Device::GetResourceTiling:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling) obtém informações sobre como um recurso lado a lado é dividido em blocos.

## <a name="related-topics"></a>Tópicos relacionados

* [Associação de recursos](resource-binding.md)
