---
title: Sombreadores de computação no hardware de nível baixo
description: Este tópico discute como usar sombreadores de computação em um aplicativo Direct3D 11 no hardware do Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673397d6974d2191acc1f5e30ccf8cae8b5b5f4b0ab5cae305360fef3e7186f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894466"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Sombreadores de computação no hardware de nível baixo

O Direct3D 11 fornece [](direct3d-11-advanced-stages-compute-shader.md) a capacidade de usar sombreadores de computação que operam na maioria dos hardwares direct3D 10.x, com algumas limitações de operação. A tecnologia de sombreador de computação também é conhecida como a tecnologia DirectCompute. Este tópico discute como usar [](direct3d-11-advanced-stages-compute-shader.md) sombreadores de computação em um aplicativo Direct3D 11 no hardware do Direct3D 10.

O suporte para sombreadores de computação em hardware de nível baixo é apenas para dispositivos compatíveis com o Direct3D 10.x. Os sombreadores de computação não podem ser usados no hardware direct3D 9.x.

Para verificar se o hardware direct3D 10.x dá suporte a sombreadores de computação, chame [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Na chamada **CheckFeatureSupport,** passe o valor D3D11 FEATURE D3D10 X HARDWARE OPTIONS para o parâmetro Feature, passe um ponteiro para a estrutura \_ \_ \_ \_ \_ [**D3D11 \_ FEATURE \_ DATA \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) para o  parâmetro *pFeatureSupportData* e passe o tamanho da estrutura **D3D11 FEATURE DATA \_ \_ \_ D3D10 X OPÇÕES \_ \_ \_** DE HARDWARE para o parâmetro *FeatureSupportDataSize.* **CheckFeatureSupport** retornará **TRUE** no membro **ComputeShaders \_ Plus \_ RawAndStructuredBuffers via \_ \_ Sombreador \_ 4 \_ x** de **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS** se o hardware Direct3D 10.x for compatível com sombreadores de computação.

A seção [Referência 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre como vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportam em vários níveis de recurso 10Level9.

-   [Exibições de acesso não organizado (UAVs)](#unordered-access-views-uavs)
-   [Exibições de recursos do sombreador (SRVs)](#shader-resource-views-srvs)
-   [Grupos de Threads](#thread-groups)
    -   [Dimensões do grupo de threads](#thread-group-dimensions)
    -   [Índices de thread bidimensionais](#two-dimensional-thread-indices)
    -   [TGSM (Memória Compartilhada do Grupo de Threads)](#thread-group-shared-memory-tgsm)
-   [D3DCompile com OTIMIZAÇÃO DE IGNORAR D3DCOMPILE \_ \_](/windows)
-   [Tópicos relacionados](#related-topics)

## <a name="unordered-access-views-uavs"></a>Exibições de acesso não organizado (UAVs)

Raw ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) e Structured ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) Exibições de acesso não organizado têm suporte em hardware de nível baixo, com as seguintes limitações:

-   Somente um único UAV pode ser vinculado a um pipeline por vez por [**meio de ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   O deslocamento de base para um UAV bruto deve ser alinhado em um limite de 256 byte (em vez do alinhamento de 16 byte necessário para hardware Direct3D 11).

Não há suporte para UAVs digitados em hardware de nível baixo. Isso inclui [UAVs Texture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)e [Texture3D.](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

Sombreadores de pixel em hardware de nível baixo não são suportados para acesso não organizado.

## <a name="shader-resource-views-srvs"></a>Exibições de recursos do sombreador (SRVs)

Buffers brutos e estruturados como exibições de recurso do sombreador têm suporte em hardware de nível baixo para acesso somente leitura, pois estão no hardware direct3D 11. Esses tipos de recursos têm suporte para sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, bem como sombreadores de computação.

## <a name="thread-groups"></a>Grupos de Threads

Um sombreador de computação pode ser executado em muitos threads em paralelo, dentro de um grupo de threads.

Há suporte para grupos de threads em hardware de nível baixo, com as seguintes limitações:

### <a name="thread-group-dimensions"></a>Dimensões do grupo de threads

Os grupos de threads definidos para hardware de nível baixo são limitados às dimensões X e Y de 768. Isso é menor que os valores máximos de 1024 para hardware Direct3D 11. A dimensão Z máxima de 64 permanece inalterada.

O número total de threads no grupo (X × Y × Z) é limitado a 768. Isso é menor que o limite de 1024 para hardware direct3D 11.

Se esses números são excedido, a compilação do sombreador falhará.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional índices de thread de Two-Dimensional

Um thread específico dentro de um grupo de threads é indexado usando um vetor 3D dado por (x,y,z).

Para sombreadores de computação que operam em hardware de nível baixo, os grupos de threads só suportam duas dimensões. Isso significa que o valor Z no vetor 3D sempre deve ser 1.

Essa limitação se aplica especificamente ao seguinte:

-   [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)— o *argumento ThreadGroupCountZ* deve ser 1.
-   [**ID3D11DeviceContext::D ispatchIndirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)— Essa função não tem suporte em hardware de nível baixo.
-   [numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)— o valor Z deve ser 1.

### <a name="thread-group-shared-memory-tgsm"></a>TGSM (Memória Compartilhada do Grupo de Threads)

A Memória Compartilhada do Grupo de Threads é limitada a 16Kb em hardware de nível baixo. Isso é menor que os 32Kb que estão disponíveis para o hardware direct3D 11.

Um thread do Sombreador de Computação só pode gravar em sua própria região do TGSM. Essa região somente gravação tem um tamanho máximo de 256 bytes ou menos, com o máximo diminuindo conforme o número de threads declarados para o grupo aumenta.

A tabela a seguir define o tamanho máximo por thread de uma região TGSM para o número de threads no grupo:



| Número de threads no grupo | Tamanho máximo de TGSM por thread |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

Um thread do Sombreador de Computação pode ler o TGSM de qualquer local.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile com OTIMIZAÇÃO DE IGNORAR D3DCOMPILE \_ \_

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) retorna **E \_ NOTIMPL** quando você passa cs 4 0 como o destino do sombreador junto com a opção de \_ \_ compilação [**D3DCOMPILE \_ SKIP \_ OPTIMIZATION.**](/windows/desktop/direct3dhlsl/d3dcompile-constants) O destino do sombreador cs \_ \_ 5 0 funciona com **A OTIMIZAÇÃO DE \_ \_ SKIP de D3DCOMPILE.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D 11 no hardware de nível baixo](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 