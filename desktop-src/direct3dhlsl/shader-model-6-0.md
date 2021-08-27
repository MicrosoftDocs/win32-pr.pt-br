---
title: Modelo do sombreador 6
description: O Shader Model 6,0 adiciona uma variedade de intrínsecores de operação de onda para o pixel e sombreadores de computação.
ms.assetid: 2F28F86D-F599-47EA-90D7-6833ABA976FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609f0a9d36fbf7414e724cd31bc05a8e4d6abdefa5c842f30934feba0dffb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790695"
---
# <a name="shader-model-6"></a>Modelo do sombreador 6

Todos os Intrínsecores de ondas não relacionados ao Quad estão disponíveis em todos os estágios de sombreador. Os intrínsecos do Quad Wave estão disponíveis somente em sombreadores de computação e pixel.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                 | Descrição                                                                                                                                                               |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QuadReadAcrossDiagonal**](quadreadacrossdiagonal.md)<br/> | Retorna o valor local especificado que é lido da pista na diagonal oposta neste Quad.<br/>                                                                |
| [**QuadReadLaneAt**](quadreadlaneat.md)<br/>                   | Retorna o valor de origem especificado da pista identificada pela ID da pista dentro do Quad atual.<br/>                                                            |
| [**QuadReadAcrossX**](quadswapx.md)<br/>                      | Retorna o valor local especificado lido da outra pista neste Quad na direção X.<br/>                                                                    |
| [**QuadReadAcrossY**](quadswapy.md)<br/>                      | Retorna o valor de origem especificado lido da outra pista neste Quad na direção Y.<br/>                                                                   |
| [**WaveActiveAllEqual**](waveactiveallequal.md)<br/>           | Retornará true se a expressão for a mesma para cada pista ativa na onda atual (e, portanto, uniforme em toda a ti).<br/>                                             |
| [**WaveActiveBitAnd**](waveallbitand.md)<br/>                  | Retorna o bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas. <br/>           |
| [**WaveActiveBitOr**](waveallbitor.md)<br/>                    | Retorna o valor de bit e de todos os valores da expressão em todas as pistas ativas na onda atual e os Replica de volta para todas as pistas ativas. <br/>            |
| [**WaveActiveBitXor**](waveallbitxor.md)<br/>                  | Retorna o XOR bit a bit de todos os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas. <br/>           |
| [**WaveActiveCountBits**](waveactivecountbits.md)<br/>         | Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda.<br/> |
| [**WaveActiveMax**](waveallmax.md)<br/>                        | Retorna o valor máximo da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas. <br/>                           |
| [**WaveActiveMin**](waveallmin.md)<br/>                        | Retorna o valor mínimo da expressão em todas as pistas ativas na onda atual, replicando-a de volta para todas as pistas ativas. <br/>                               |
| [**WaveActiveProduct**](waveallproduct.md)<br/>                | Multiplica os valores da expressão em todas as pistas ativas na onda atual e a Replica de volta para todas as pistas ativas.<br/>                       |
| [**WaveActiveSum**](waveallsum.md)<br/>                        | Soma o valor da expressão em todas as pistas ativas na onda atual e a Replica para todas as pistas na onda atual.<br/>                            |
| [**WaveActiveAllTrue**](wavealltrue.md)<br/>                   | Retornará true se a expressão for verdadeira em todas as pistas ativas na onda atual.<br/>                                                                                |
| [**WaveActiveAnyTrue**](waveanytrue.md)<br/>                   | Retornará true se a expressão for verdadeira em qualquer uma das pistas ativas na onda atual.<br/>                                                                         |
| [**WaveActiveBallot**](waveballot.md)<br/>                     | Retorna um bitmask de inteiro sem sinal de 4 bits da avaliação da expressão booliana para todas as pistas ativas na onda especificada. <br/>                              |
| [**WaveGetLaneCount**](wavegetlanecount.md)<br/>               | Retorna o número de pistas em uma onda nessa arquitetura. <br/>                                                                                                   |
| [**WaveGetLaneIndex**](wavegetlaneindex.md)<br/>               | Retorna o índice da pista atual dentro da onda atual. <br/>                                                                                                |
| [**WaveIsFirstLane**](waveisfirstlane.md)<br/>                 | Retorna true somente para a pista ativa na onda atual com o menor índice. <br/>                                                                            |
| [**WavePrefixCountBits**](waveprefixcountbytes.md)<br/>        | Retorna a soma de todas as variáveis boolianas especificadas definidas como true em todas as pistas ativas com índices menores que a raia atual. <br/>                        |
| [**WavePrefixProduct**](waveprefixproduct.md)<br/>             | Retorna o produto de todos os valores nas pistas ativas nesta onda com índices menores que esta raia.<br/>                                                    |
| [**WavePrefixSum**](waveprefixsum.md)<br/>                     | Retorna a soma de todos os valores nas pistas ativas com índices menores do que este.<br/>                                                                   |
| [**WaveReadLaneFirst**](wavereadfirstlane.md)<br/>             | Retorna o valor da expressão para a pista ativa da onda atual com o menor índice. <br/>                                                          |
| [**WaveReadLaneAt**](wavereadlaneat.md)<br/>                   | Retorna o valor da expressão para o índice de raia fornecido dentro da onda especificada.<br/>                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do modelo do sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 





