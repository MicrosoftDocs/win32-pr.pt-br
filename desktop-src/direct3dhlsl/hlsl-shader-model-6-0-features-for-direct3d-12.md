---
title: Modelo 6.0 do Sombreador HLSL
description: Descreve os intrínsecos de operação de onda adicionados ao Modelo de Sombreador HLSL 6.0.
ms.assetid: BF968CD3-AC67-48DB-B93F-EF54B680106F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f0f06050c4c387b8e50c1c0cfb39dc5689d45d0e31bd7df5a81f45c63815a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986536"
---
# <a name="hlsl-shader-model-60"></a>Modelo 6.0 do Sombreador HLSL

Descreve os intrínsecos de operação de onda adicionados ao Modelo de Sombreador HLSL 6.0.

- [Modelo de sombreador 6.0](#shader-model-60)
- [Terminologia](#terminology)
- [Intrínsecos de linguagem de sombreamento](#shading-language-intrinsics)
    - [Consulta wave](#wave-query)
    - [Wave Vote](#wave-vote)
    - [Difusão de onda](#wave-broadcast)
    - [Redução de onda](#wave-reduction)
    - [Verificação de onda e prefixo](#wave-scan-and-prefix)
    - [Operações aleatórias de todo o quádruplo](#quad-wide-shuffle-operations)
- [Funcionalidade de hardware](#hardware-capability)
- [Tópicos relacionados](#related-topics)

## <a name="shader-model-60"></a>Modelo de sombreador 6.0

Para modelos de sombreador anteriores, a programação HLSL expõe apenas um único thread de execução. Novas operações de nível de onda são fornecidas, começando com o modelo 6.0, para aproveitar explicitamente o paralelismo das GPUs atuais – muitos threads podem ser executados em lockstep no mesmo núcleo simultaneamente. Por exemplo, os intrínsecos do modelo 6.0 permitem a eliminação de constructos de barreira quando o escopo da sincronização está dentro da largura do processador SIMD ou algum outro conjunto de threads que são conhecidos como atômicos em relação uns aos outros.

Os possíveis casos de uso incluem: compactação de fluxo, reduções, transposição de blocos, classificação bitônica ou FFT (Fast Fourier Transforms), binning, des duplicação de fluxo e cenários semelhantes.

A maioria dos intrínsecos aparece em sombreadores de pixel e sombreadores de computação, embora haja algumas exceções (notadas para cada função). As funções foram adicionadas aos requisitos do DirectX Feature Level 12.0, no nível da API 12.

O parâmetro e o valor de retorno para essas funções implicam o tipo da expressão, os tipos com suporte são aqueles da lista a seguir que também estão presentes no modelo de sombreador de destino para *<type>* seu aplicativo: 

- half, half2, half3, half4
- float, float2, float3, float4
- double, double2, double3, double4
- int, int2, int3, int4
- uint, uint2, uint3, uint4
- short, short2, short3, short4
- ushort, ushort2, ushort3, ushort4
- uint64 \_ t, uint64 \_ t2, uint64 \_ t3, uint64 \_ t4

Algumas operações (como os operadores bit a bit) só suportam os tipos inteiros.

## <a name="terminology"></a>Terminologia

| **Termo** | **Definição** |
|-|-|
| Pista | Um único thread de execução. Os modelos de sombreador anteriores à versão 6.0 expõem apenas um deles no nível da linguagem, deixando a expansão para o processamento de SIMD paralelo totalmente até a implementação. |
| Wave | Um conjunto de pistas (threads) executado simultaneamente no processador. Nenhuma barreira explícita é necessária para garantir que elas sejam executadas em paralelo. Conceitos semelhantes incluem "distorção" e "wavefront". |
| Inativo Lane | Uma faixa que não está sendo executada, por exemplo, devido ao fluxo de controle ou trabalho insuficiente para preencher o tamanho mínimo da onda. |
| Faixa ativa | Uma faixa para a qual a execução está sendo executada. Em sombreadores de pixel, ele pode incluir qualquer faixa de pixel auxiliar. |
| Quad | Um conjunto de 4 pistas adjacentes correspondentes a pixels organizados em um quadrado 2x2. Eles são usados para estimar gradientes diferenciando x ou y. Uma onda pode ser composta por vários quads. Todos os pixels em um quad ativo são executados (e podem ser "Active Lanes"), mas aqueles que não produzem resultados visíveis são termo "Helper Lanes". |
| Helper Lane | Uma faixa que é executada exclusivamente para fins de gradientes em quads de sombreador de pixel. A saída dessa faixa será descartada e, portanto, não renderizará para a superfície de destino. |

## <a name="shading-language-intrinsics"></a>Intrínsecos de linguagem de sombreamento

Todas as operações desse modelo de sombreador foram adicionadas em uma variedade de funções intrínsecas.

### <a name="wave-query"></a>Consulta wave

Os intrínsecos para consultar uma única onda.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveGetLaneCount**](wavegetlanecount.md) | Retorna o número de pistas na onda atual. | \* | \* |
| [**WaveGetLaneIndex**](wavegetlaneindex.md) | Retorna o índice da faixa atual dentro da onda atual. | \* | \* |
| [**WaveIsFirstLane**](waveisfirstlane.md) | Retorna true somente para a faixa ativa na onda atual com o menor índice | \* | \* |

### <a name="wave-vote"></a>Wave Vote

Esse conjunto de intrínsecos compara valores entre threads atualmente ativos da onda atual.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveActiveAnyTrue**](waveanytrue.md) | Retornará true se a expressão for verdadeira em qualquer faixa ativa na onda atual. | \* | \* |
| [**WaveActiveAllTrue**](wavealltrue.md) | Retornará true se a expressão for verdadeira em todas as faixas ativas na onda atual. | \* | \* |
| [**WaveActiveBallot**](waveballot.md) | Retorna uma máscara de bitmas de inteiro sem sinal de 64 bits da avaliação da expressão booliana para todas as faixas ativas na onda especificada. | \* | \* |

### <a name="wave-broadcast"></a>Difusão de onda

Esses intrínsecos permitem que todas as faixas ativas na onda atual recebam o valor da faixa especificada, transmitindo-o efetivamente. O valor de retorno de uma faixa inválida é indefinido.

| **Intrinsic** | **Descrição** | **Sombreador de pixel** | **Sombreador de computação** |
|-|-|-|-|
| [**WaveReadLaneAt**](wavereadlaneat.md) | Retorna o valor da expressão para o índice de lane especificado dentro da onda especificada. | \* | \* |
| [**WaveReadLaneFirst**](wavereadfirstlane.md) | Retorna o valor da expressão para a faixa ativa da onda atual com o menor índice. | \* | \* |

### <a name="wave-reduction"></a>Redução de onda

Esses intrínsecos computam a operação especificada em todas as faixas ativas na onda e transmitem o resultado final para todas as faixas ativas. Portanto, a saída final é garantida uniforme em toda a onda.

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

Y 


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
