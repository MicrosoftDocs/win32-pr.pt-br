---
title: Sombreadores de computação em hardware de nível inferior
description: Este tópico discute como usar sombreadores de computação em um aplicativo do Direct3D 11 no hardware do Direct3D 10.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008574"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Sombreadores de computação em hardware de nível inferior

O Direct3D 11 fornece a capacidade de usar [sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) que operam na maioria dos hardwares do Direct3D 10. x, com algumas limitações para a operação. A tecnologia de sombreador de computação também é conhecida como a tecnologia DirectCompute. Este tópico discute como usar [sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) em um aplicativo do Direct3D 11 no hardware do Direct3D 10.

O suporte para sombreadores de computação em hardware de nível inferior é apenas para dispositivos compatíveis com o Direct3D 10. x. Os sombreadores de computação não podem ser usados no hardware do Direct3D 9. x.

Para verificar se o hardware do Direct3D 10. x dá suporte a sombreadores de computação, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Na chamada **CheckFeatureSupport** , passe o valor de \_ \_ Opções de hardware d3d10 X do recurso D3D11 \_ \_ \_ para o parâmetro *Feature* , passe um ponteiro para a estrutura de [**\_ \_ \_ \_ \_ \_ Opções de hardware d3d10 x, dados do recurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) para o parâmetro pFeatureSupportData e passe o tamanho da estrutura de  opções de **\_ \_ \_ \_ \_ hardware \_ D3D11 x** para o parâmetro *d3d10* . **CheckFeatureSupport** retorna **true** no **ComputeShaders \_ Plus RawAndStructuredBuffers por meio do membro do \_ \_ \_ sombreador \_ 4 \_ x** de **D3D11 \_ recurso \_ dados \_ d3d10 \_ x \_ \_ Opções de hardware** se o hardware Direct3D 10. x der suporte a sombreadores de computação.

A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.

-   [Exibições de acesso não ordenado (UAVs)](#unordered-access-views-uavs)
-   [Exibições de recursos do sombreador (SRVs)](#shader-resource-views-srvs)
-   [Grupos de threads](#thread-groups)
    -   [Dimensões do grupo de threads](#thread-group-dimensions)
    -   [Índices de thread bidimensionais](#two-dimensional-thread-indices)
    -   [Memória compartilhada do grupo de threads (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile com D3DCOMPILE \_ ignorar \_ otimização](/windows)
-   [Tópicos relacionados](#related-topics)

## <a name="unordered-access-views-uavs"></a>Exibições de acesso não ordenado (UAVs)

As exibições de acesso não ordenado bruto ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) e estruturado ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) têm suporte em hardware de nível inferior, com as seguintes limitações:

-   Apenas um único UAV pode ser associado a um pipeline por vez por meio de [**ID3D11DeviceContext:: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews).
-   O deslocamento de base para um UAV bruto deve ser alinhado em um limite de 256 bytes (em vez de um alinhamento de 16 bytes necessário para o hardware do Direct3D 11).

Não há suporte para UAVs tipados em hardware de nível inferior. Isso inclui [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)e [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) UAVs.

Os sombreadores de pixel no hardware de nível inferior não dão suporte ao acesso não ordenado.

## <a name="shader-resource-views-srvs"></a>Exibições de recursos do sombreador (SRVs)

Buffers brutos e estruturados como exibições de recursos de sombreador têm suporte em hardware de nível inferior para acesso somente leitura, pois eles estão no hardware do Direct3D 11. Esses tipos de recursos têm suporte para sombreadores de vértice, sombreadores de geometria, sombreadores de pixel, bem como sombreadores de computação.

## <a name="thread-groups"></a>Grupos de threads

Um sombreador de computação pode ser executado em vários threads em paralelo, dentro de um grupo de threads.

Os grupos de threads têm suporte em hardware de nível inferior, com as seguintes limitações:

### <a name="thread-group-dimensions"></a>Dimensões do grupo de threads

Os grupos de threads definidos para hardware de nível inferior são limitados às dimensões X e Y de 768. Isso é menor que os valores máximos de 1024 para o hardware do Direct3D 11. A dimensão Z máxima de 64 é inalterada.

O número total de threads no grupo (X × Y × Z) é limitado a 768. Isso é menor que o limite de 1024 para o hardware do Direct3D 11.

Se esses números forem excedidos, a compilação do sombreador falhará.

### <a name="two-dimensional-thread-indices"></a>Índices de thread Two-Dimensional

Um thread específico dentro de um grupo de threads é indexado usando um vetor 3D fornecido por (x, y, z).

Para sombreadores de computação operando em hardware de nível inferior, os grupos de threads dão suporte apenas a duas dimensões. Isso significa que o valor Z no vetor 3D sempre deve ser 1.

Essa limitação se aplica especificamente ao seguinte:

-   [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)— o argumento *ThreadGroupCountZ* deve ser 1.
-   [**ID3D11DeviceContext::D ispatchindirect**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)— essa função não tem suporte em hardware de nível inferior.
-   [numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)– o valor Z deve ser 1.

### <a name="thread-group-shared-memory-tgsm"></a>Memória compartilhada do grupo de threads (TGSM)

A memória compartilhada do grupo de threads está limitada a 16 KB no hardware de nível inferior. Isso é menor do que o 32 KB que está disponível para o hardware do Direct3D 11.

Um thread de sombreador de computação só pode gravar em sua própria região de TGSM. Essa região somente gravação tem um tamanho máximo de 256 bytes ou menos, com o máximo de redução conforme o número de threads declarados para o grupo aumenta.

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



 

Um thread de sombreador de computação pode ler o TGSM de qualquer local.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile com D3DCOMPILE \_ ignorar \_ otimização

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) retorna **E \_ NOTIMPL** quando você passa cs \_ 4 \_ 0 como o destino do sombreador junto com a opção de compilação de [**\_ \_ otimização D3DCompile Skip**](/windows/desktop/direct3dhlsl/d3dcompile-constants) . O \_ destino do \_ sombreador CS 5 0 funciona com a **\_ \_ otimização D3DCOMPILE Skip**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 