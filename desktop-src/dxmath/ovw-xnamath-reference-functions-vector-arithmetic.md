---
description: Lista as funções aritméticas de vetor.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Funções aritméticas de vetor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ad5149153b736ddf6d2f2af5b9671e32651f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785234"
---
# <a name="vector-arithmetic-functions"></a>Funções aritméticas de vetor

Lista as funções aritméticas de vetor.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Computa o valor absoluto de cada componente de um [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Computa a soma de dois vetores.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Adiciona dois vetores representando ângulos.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Computa o teto de cada componente de um [**XMVECTOR**](xmvector-data-type.md).<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Coloca os componentes de um vetor para um intervalo mínimo e máximo especificado.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divide uma instância do `XMVECTOR` por uma segunda instância, retornando o resultado em uma terceira instância.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Computa o andar de cada componente de um [**XMVECTOR**](xmvector-data-type.md).<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Executa um teste por componente para +/-infinito em um vetor.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Executa um teste NaN por componente em um vetor.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Faz uma comparação por componente entre dois vetores e retorna um vetor contendo os maiores componentes.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Faz uma comparação por componente entre dois vetores e retorna um vetor contendo os menores componentes.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Computa o restante do ponto flutuante por componente do quociente de dois vetores.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Computa o 2PI de módulo de ângulo por componente.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Computa o produto por componente de dois vetores.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Computa o produto dos dois primeiros vetores adicionados ao terceiro vetor.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Computa a negação de um vetor.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Computa a diferença de um terceiro vetor e o produto dos dois primeiros vetores.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | As computações *v1* são elevadas para a potência de *v2*.<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Computa o recíproco por componente de um vetor.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Estima o recíproco por componente de um vetor.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Computa a raiz quadrada recíproca por componente de um vetor.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Estima a raiz quadrada recíproca por componente de um vetor.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Arredonda cada componente de um vetor para o número inteiro mais próximo.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Satura cada componente de um vetor para o intervalo de 0,0 a 1,0 f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Escalar multiplica um vetor por um valor de ponto flutuante.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Computa a raiz quadrada por componente de um vetor.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Estima a raiz quadrada por componente de um vetor.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Computa a diferença de dois vetores.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Subtrai dois vetores que representam ângulos.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Computa a soma horizontal dos componentes de um [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Arredonda cada componente de um vetor para o valor inteiro mais próximo na direção de zero.<br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de vetor da biblioteca DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
