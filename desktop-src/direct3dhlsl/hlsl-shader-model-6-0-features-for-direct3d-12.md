---
title: Modelo de sombreador HLSL 6,0
description: Descreve os intrínsecores de operação de onda adicionados ao modelo de sombreador HLSL 6,0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e55661e3f91125597c8c7842a1be16129cefe0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995463"
---
# <a name="hlsl-shader-model-60"></a>Modelo de sombreador HLSL 6,0

Descreve os intrínsecores de operação de onda adicionados ao modelo de sombreador HLSL 6,0.

- [Modelo do sombreador 6,0](#shader-model-60)
- [Terminologia](#terminology)
- [Intrínsecos da linguagem de sombreamento](#shading-language-intrinsics)
    - [Consulta de onda](#wave-query)
    - [Voto de onda](#wave-vote)
    - [Difusão de ondas](#wave-broadcast)
    - [Redução de onda](#wave-reduction)
    - [Verificação de onda e prefixo](#wave-scan-and-prefix)
    - [Operações de ordem aleatória quádrupla](#quad-wide-shuffle-operations)
- [Funcionalidade de hardware](#hardware-capability)
- [Tópicos relacionados](#related-topics)

## <a name="shader-model-60"></a>Modelo do sombreador 6,0

Para modelos de sombreador anteriores, a programação HLSL expõe apenas um único thread de execução. Novas operações de nível Wave são fornecidas, começando com o modelo 6,0, para aproveitar explicitamente o paralelismo de GPUs atuais – muitos threads podem ser executados em atrelada no mesmo núcleo simultaneamente. Por exemplo, os intrínsecos do modelo 6,0 permitem a eliminação de construções de barreira quando o escopo da sincronização está dentro da largura do processador SIMD ou de algum outro conjunto de threads que são conhecidos como atômicos em relação uns aos outros.

Os casos de uso em potencial incluem: compactação de fluxo, reduções, bloquear Transpose, classificação de bitônico ou transformações de Fourier rápidas (FFT), compartimentalização, eliminação de duplicação de fluxo e cenários semelhantes.

A maioria dos intrínsecores aparece em sombreadores de pixel e sombreadores de computação, embora haja algumas exceções (indicadas para cada função). As funções foram adicionadas aos requisitos para o nível de recurso do DirectX 12,0, sob API nível 12.

O *<type>* parâmetro e o valor de retorno para essas funções implicam no tipo da expressão, os tipos com suporte são os da lista a seguir que *também* estão presentes no modelo de sombreador de destino para seu aplicativo:

- metade, half2, half3, half4
- float, float2, float3, FLOAT4
- Double, double2, double3, double4
- int, Int2, Int3, INT4
- uint, uint2, uint3, uint4
- Short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- UInt64 \_ t, UInt64 \_ T2, UInt64 \_ T3, UInt64 \_ T4

Algumas operações (tais como os operadores bit a bit) dão suporte apenas a tipos inteiros.

## <a name="terminology"></a>Terminologia

| **Termo** | **Definição** |
|-|-|
| Estreita | Um único thread de execução. Os modelos de sombreador antes da versão 6,0 expõem apenas um deles no nível de linguagem, deixando a expansão para o processamento paralelo de SIMD inteiramente na implementação. |
| Wave | Um conjunto de pistas (threads) executado simultaneamente no processador. Não são necessárias barreiras explícitas para garantir que elas sejam executadas em paralelo. Conceitos semelhantes incluem "Warp" e "Wavefront". |
| Raia inativa | Uma pista que não está sendo executada, por exemplo, devido ao fluxo de controle ou trabalho insuficiente para preencher o tamanho mínimo da onda. |
| Pista ativa | Uma pista para a qual a execução está sendo executada. Em sombreadores de pixel, ele pode incluir pistas de pixel auxiliares. |
| Quadra | Um conjunto de 4 pistas adjacentes correspondentes a pixels organizados em um quadrado 2x2. Eles são usados para estimar gradientes por diferenciação em x ou y. Uma onda pode ser composta por vários quatro processadores. Todos os pixels em um quad ativo são executados (e podem ser "pistas ativas"), mas aqueles que não produzem resultados visíveis são chamados de "pistas auxiliares". |
| Pista auxiliar | Uma pista que é executada exclusivamente para fins de gradientes no sombreador de pixel quads. A saída de tal raia será descartada e, portanto, não renderizará para a superfície de destino. |

## <a name="shading-language-intrinsics"></a>Intrínsecos da linguagem de sombreamento

Todas as operações desse modelo de sombreador foram adicionadas em uma variedade de funções intrínsecas.

### <a name="wave-query"></a>Consulta de onda

Os intrínsecos para consultar uma única onda.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Retorna o número de pistas na onda atual. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Retorna o índice da pista atual dentro da onda atual. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Retorna true somente para a pista ativa na onda atual com o menor índice | \* | \* |

### <a name="wave-vote"></a>Voto de onda

Esse conjunto de intrínsecos compara valores entre threads atualmente ativos da onda atual.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Retornará true se a expressão for verdadeira em qualquer rota ativa na onda atual. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Retornará true se a expressão for verdadeira em todas as pistas ativas na onda atual. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Retorna um bitmask de inteiro sem sinal de 64 bits da avaliação da expressão booliana para todas as pistas ativas na onda especificada. | \* | \* |

### <a name="wave-broadcast"></a>Difusão de ondas

Esses intrínsecos permitem que todas as pistas ativas na onda atual recebam o valor da pista especificada, transmitindo-a efetivamente. O valor de retorno de uma pista inválida é indefinido.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Retorna o valor da expressão para a pista ativa da onda atual com o menor índice. | \* | \* |

### <a name="wave-reduction"></a>Redução de onda

Esses intrínsecos computam a operação especificada em todas as pistas ativas na onda e transmitem o resultado final para todas as pistas ativas. Portanto, a saída final é garantida uniforme em toda a onda.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveActiveAllEqual**](waveactiveallequal.md) | Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti). | \* | \* |
| [**WaveActiveBitAnd**](waveallbitand.md) | Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveBitOr**](waveallbitor.md) | Retorna o valor de bit e de todos os valores da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveBitXor**](waveallbitxor.md) | Retorna a seqüência de bits exclusiva ou de todos os valores da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveCountBits**](waveactivecountbits.md) | Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveMax**](waveallmax.md) | Computa o valor máximo da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveMin**](waveallmin.md) | Computa o valor mínimo da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveProduct**](waveallproduct.md) | Multiplica os valores da expressão em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |
| [**WaveActiveSum**](waveallsum.md) | Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual e replica o resultado para todas as pistas na onda. | \* | \* |

### <a name="wave-scan-and-prefix"></a>Verificação de onda e prefixo

Esses intrínsecos aplicam a operação a cada raia e deixam cada resultado parcial da computação na pista correspondente.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WavePrefixCountBits**](waveprefixcountbytes.md) | Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual. | \* | \* |
| [**WavePrefixSum**](waveprefixsum.md) | Retorna a soma de todos os valores nas pistas ativas com índices menores do que este. | \* | \* |
| [**WavePrefixProduct**](waveprefixproduct.md) | Retorna o produto de todos os valores nas pistas antes desta de uma onda especificada. | \* | \* |

### <a name="quad-wide-shuffle-operations"></a>Operações de ordem aleatória quádrupla

Esses intrínsecos executam operações de permuta nos valores em uma onda conhecida por conter quatro sombreadores de pixel, conforme definido aqui. Os índices dos pixels no Quad são definidos na linha de varredura ou na ordem de leitura-onde as coordenadas em um quad são:

+---------> X 

| [0] [1] 

| [2] [3] 

v 

S 


Essas rotinas funcionam em sombreadores de computação ou sombreadores de pixel. Em sombreadores de computação eles operam em quatro processadores definidos como grupos de 4 divididos uniformemente em uma onda de SIMD. Em sombreadores de pixel eles devem ser usados em ondas capturadas por WaveQuadLanes, caso contrário os resultados são indefinidos.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**QuadReadLaneAt**](quadreadlaneat.md) | Retorna o valor de origem especificado lido da pista do quádruplo atual identificado por quadLaneID \[ 0.. 3, \] que deve ser uniforme em todo o quad. | \* | |
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md) | Retorna o valor local especificado que é lido da pista na diagonal oposta neste Quad. | \* | |
| [**QuadReadAcrossX**](quadswapx.md) | Retorna o valor de origem especificado lido da outra pista neste Quad na direção X. | \* | |
| [**QuadReadAcrossY**](quadswapy.md) | Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y. | \* | |

## <a name="hardware-capability"></a>Funcionalidade de hardware

Para verificar se os recursos de operação de onda estão disponíveis em qualquer hardware específico, chame [**ID3D12Device:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport), observando a descrição e o uso da estrutura [**de \_ dados do recurso D3D12 \_ \_ D3D12 \_ OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1) .

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
* [Modelo de sombreador 6 intrínsecos](shader-model-6-0.md)
