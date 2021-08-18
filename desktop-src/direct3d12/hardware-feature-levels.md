---
title: Níveis de recursos de hardware
description: Descreve a funcionalidade dos 11 \_ 0 a 12 \_ 1 níveis de recursos de hardware.
ms.assetid: B8304E29-A532-464E-8FAF-075228D8FB73
keywords:
- Nível de recurso DX
- Nível de recursos do DirectX
- nível de recurso, DX
- nível de recurso, DirectX
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf069baca3d9ff56c0d3d98e79bb553df7e8acf1fadf7b5888c5b5d211f7a874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124144"
---
# <a name="hardware-feature-levels"></a>Níveis de recursos de hardware

Descreve a funcionalidade dos 11 \_ 0 a 12 \_ 1 níveis de recursos de hardware.

-   [Sistemas de numeração](#numbering-systems)
-   [Suporte de nível de recurso](#feature-level-support)
-   [Suporte de hardware para formatos DXGI](#hardware-support-for-dxgi-formats)
-   [Tópicos relacionados](#related-topics)

Para lidar com a diversidade de placas de vídeo em máquinas novas e existentes, o Microsoft Direct3D 11 introduziu o conceito de níveis de recursos. Cada placa de vídeo implementa um certo nível de funcionalidade DX (Microsoft DirectX), dependendo das GPUs (unidades de processamento gráfico) instaladas. Um nível de recurso é um conjunto bem definido de funcionalidades de GPU. Por exemplo, o nível de recurso de 11 \_ 0 implementa a funcionalidade que foi implementada no Direct3D 11.

Agora, ao criar um dispositivo, você pode tentar criar um dispositivo para o nível de recurso que deseja solicitar. Se for possível criar um dispositivo, isso significa que o nível de recursos existe; caso contrário, o hardware não permite tal nível de recursos. Você pode tentar recriar um dispositivo em um nível de recursos inferior ou optar por sair do aplicativo.

As propriedades básicas dos níveis de recursos são:

-   Todos os drivers do Direct3D 12 serão de nível \_ de recurso 11 0 ou melhor.
-   Uma GPU que permite a criação de um dispositivo atende ou excede a funcionalidade desse nível de recurso.
-   Um nível de recurso sempre inclui a funcionalidade dos níveis de recursos anteriores ou inferiores.
-   Um nível de recurso não implica o desempenho, apenas a funcionalidade. O desempenho depende da implementação de hardware.
-   Um nível de recurso é escolhido quando você chama [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice).
-   Para obter informações mais detalhadas sobre os recursos com suporte (especialmente aqueles marcados como *opcional* na tabela abaixo, o que significa que o hardware pode dar suporte ao recurso, mas não é necessário) chamar [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

Para obter informações sobre limitações na criação de dispositivos de tipo não hardware em determinados níveis de recursos, consulte [limitações criando dispositivos de referência e detorção](/windows/desktop/direct3d11/overviews-direct3d-11-devices-limitations). Para obter mais informações sobre a introdução dos níveis de recurso, consulte a documentação do Direct3D 11 em [níveis de recurso do Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).

## <a name="numbering-systems"></a>Sistemas de numeração

Os níveis de recursos de hardware *não* são os mesmos que as versões de API. Por exemplo, há uma API do D3D 11.3, mas não há 11 \_ 3 níveis de recurso de hardware. Os níveis de recurso são definidos na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) .

Há três sistemas de numeração distintos:

-   As versões do Direct3D usam um ponto; por exemplo, Direct3D 12,0.
-   Os modelos de sombreador usam um ponto; por exemplo, o modelo de sombreador 5,1.
-   Os níveis de recurso usam um sublinhado; por exemplo, nível de recurso 12 \_ 0.

## <a name="feature-level-support"></a>Suporte de nível de recurso

Os recursos a seguir estão disponíveis para cada nível de recurso do Direct3D.

Os títulos na linha superior são os níveis de recurso do Direct3D. Os cabeçalhos na coluna à esquerda são recursos.



| Nível de recurso de recurso \\                                                                                                 | 12 \_ 1 ⁰                    | 12 \_ 0 ⁰                    | 11 \_ 1 ¹                   | 11 \_ 0                    |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------|---------------------------|--------------------------|--------------------------|
| Modelo de Sombreador                                                                                                             | 5.1                       | 5.1                       | 5,1 ²                     | 5,1 ²                     |
| [Camada de associação de recursos](hardware-support.md)                                                                            | Tier2 ³                    | Tier2 ³                    | Nível 1 ³                   | Nível 1 ³                   |
| [Recursos em ladrilho](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)                                                                        | Tier2 ³                    | Tier2 ³                    | Opcional                 | Opcional                 |
| [Rasterização conservativa](conservative-rasterization.md)                                                             | Nível 1 ³                    | Opcional                  | Opcional                 | Não                       |
| [Modos de exibição ordenados do rasterizador](rasterizer-order-views.md)                                                                   | Sim                       | Opcional                  | Opcional                 | Não                       |
| [Filtros mín./máx.](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter)                                                                                      | Sim                       | Sim                       | Opcional                 | Não                       |
| Mapear buffer padrão                                                                                                       | Opcional                  | Opcional                  | Opcional                 | Opcional                 |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md)                                 | Opcional                  | Opcional                  | Opcional                 | Não                       |
| [Cargas de exibição de acesso não ordenado digitado](typed-unordered-access-view-loads.md)                                               | 18 formatos, mais opcional | 18 formatos, mais opcional | 3 formatos, mais opcionais | 3 formatos, mais opcionais |
| [Sombreador de geometria](/previous-versions//bb205146(v=vs.85)) | Sim                       | Sim                       | Sim                      | Sim                      |
| [Saída de fluxo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage)                                            | Sim                       | Sim                       | Sim                      | Sim                      |
| [Sombreador DirectCompute/Compute](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)                                  | Sim                       | Sim                       | Sim                      | Sim                      |
| [Envoltória e sombreadores de domínio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                                           | Sim                       | Sim                       | Sim                      | Sim                      |
| [Matrizes de recursos de textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sim                       | Sim                       | Sim                      | Sim                      |
| [Matrizes de recursos cubemap](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-intro)                                     | Sim                       | Sim                       | Sim                      | Sim                      |
| [Compactação de BC1 a BC7](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)                        | Sim                       | Sim                       | Sim                      | Sim                      |
| [De alfa para cobertura](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-blend-state)         | Sim                       | Sim                       | Sim                      | Sim                      |
| [Operações lógicas (mesclagem de saída)](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                                          | Sim                       | Sim                       | Sim                      | Opcional                 |
| Rasterização independente de destino                                                                                         | Sim                       | Sim                       | Sim                      | Não                       |
| [Destino de renderização múltipla (MRT) com ForcedSampleCount 1](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                      | Sim                       | Sim                       | Sim                      | Opcional                 |
| [Contagem máxima de amostras forçada para renderização somente UAV](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options)                            | 16                        | 16                        | 16                       | 8                        |
| Dimensão de textura máxima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Dimensão cubemap máxima                                                                                                    | 16384                     | 16384                     | 16384                    | 16384                    |
| Extensão máxima do volume                                                                                                        | 2.048                      | 2.048                      | 2.048                     | 2.048                     |
| Repetição máxima de textura                                                                                                       | 16384                     | 16384                     | 16384                    | 16384                    |
| Anisotropy máx.                                                                                                           | 16                        | 16                        | 16                       | 16                       |
| Contagem máxima de primitivas                                                                                                      | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Índice de vértice máximo                                                                                                         | 2 ^ 32 – 1                  | 2 ^ 32 – 1                  | 2 ^ 32 – 1                 | 2 ^ 32 – 1                 |
| Máximo de Slots de entrada                                                                                                          | 32                        | 32                        | 32                       | 32                       |
| Destinos de renderização simultânea                                                                                              | 8                         | 8                         | 8                        | 8                        |
| Consultas do oclusão                                                                                                        | Sim                       | Sim                       | Sim                      | Sim                      |
| Combinação alfa separada                                                                                                     | Sim                       | Sim                       | Sim                      | Sim                      |
| Espelhar uma vez                                                                                                              | Sim                       | Sim                       | Sim                      | Sim                      |
| Sobrepondo elementos de vértice                                                                                              | Sim                       | Sim                       | Sim                      | Sim                      |
| Máscaras de Gravação Independentes                                                                                                  | Sim                       | Sim                       | Sim                      | Sim                      |
| Instanciação                                                                                                               | Sim                       | Sim                       | Sim                      | Sim                      |



 

-   Requer o runtime direct3D 11.3 ou Direct3D 12.
-   8 Requer o runtime do Direct3D 11.1.
-   Opcionalmente, o modelo de sombreador 5.0 pode dar suporte a sombreadores de precisão dupla, sombreadores de precisão dupla estendidos, a instrução **sombreador SAD4** e sombreadores de precisão parcial. Para determinar as opções do modelo de sombreador 5.0 disponíveis, chame [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport). Alguma compatibilidade depende de qual hardware você está executando: o modelo de sombreador 5.1 só tem suporte em hardware que dá suporte à API do DirectX 12, independentemente do nível de recurso que está sendo usado. O hardware do DirectX 11 dá suporte apenas ao modelo de sombreador 5.0. A API do DirectX 12 só vai para o nível de recurso 11 \_ 0.
-   As camadas superiores são opcionais.
-   Os níveis de recurso 12 0 e 12 1 exigem o \_ \_ runtime direct3D 11.3 ou Direct3D 12.
-   O nível de recurso \_ 11 1 requer o runtime do Direct3D 11.1.
-   O nível de recurso \_ 11 0 requer o runtime do Direct3D 11.0.

## <a name="hardware-support-for-dxgi-formats"></a>Suporte de hardware para formatos DXGI

Para exibir tabelas de formatos DXGI e recursos de hardware, consulte:

-   [Suporte ao formato DXGI para hardware de nível de recurso 12.1 do Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
-   [Suporte ao formato DXGI para hardware de nível de recurso 12.0 do Direct3D](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
-   [Suporte ao formato DXGI para hardware de nível de recurso 11.1 do Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
-   [Suporte ao formato DXGI para hardware de nível de recurso 11.0 do Direct3D](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
-   [Suporte de hardware para formatos Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Suporte de hardware para formatos Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consulta de funcionalidade](capability-querying.md)
</dt> <dt>

[Introdução ao Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 
