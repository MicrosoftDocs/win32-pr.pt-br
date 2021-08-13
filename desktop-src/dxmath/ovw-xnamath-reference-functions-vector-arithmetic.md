---
description: Lista as funções aritméticas vetoriais.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Funções aritméticas vetoriais
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783e60ad3ca17b7394fc801baaeedd61d89649b2f4ae5ccd3b3fa7e774ff6a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118500346"
---
# <a name="vector-arithmetic-functions"></a>Funções aritméticas vetoriais

Lista as funções aritméticas vetoriais.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Calcula o valor absoluto de cada componente de [**um XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Calcula a soma de dois vetores.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Adiciona dois vetores que representam ângulos.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Calcula o limite máximo de cada componente de [**um XMVECTOR.**](xmvector-data-type.md)<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Fixa os componentes de um vetor a um intervalo mínimo e máximo especificado.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divide uma instância de `XMVECTOR` por uma segunda instância, retornando o resultado em uma terceira instância.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Calcula o piso de cada componente de um [**XMVECTOR.**](xmvector-data-type.md)<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Executa um teste por componente para +/- infinito em um vetor.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Executa um teste de NaN por componente em um vetor.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Faz uma comparação por componente entre dois vetores e retorna um vetor que contém os maiores componentes.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Faz uma comparação por componente entre dois vetores e retorna um vetor que contém os menores componentes.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Calcula o restante do ponto flutuante por componente do quociente de dois vetores.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Calcula o módulo de ângulo por componente 2PI.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Calcula o produto por componente de dois vetores.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Calcula o produto dos dois primeiros vetores adicionados ao terceiro vetor.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Calcula a negação de um vetor.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Calcula a diferença de um terceiro vetor e o produto dos dois primeiros vetores.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Calcula *a V1 elevada* à potência de *V2.*<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Calcula a recíproca por componente de um vetor.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Estima a recíproca por componente de um vetor.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Calcula a raiz quadrada recíproca por componente de um vetor.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Estima a raiz quadrada recíproca por componente de um vetor.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Arredoda cada componente de um vetor para o inteiro mais próximo.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Satura cada componente de um vetor para o intervalo de 0,0f a 1,0f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Escalar multiplica um vetor por um valor de ponto flutuante.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Calcula a raiz quadrada por componente de um vetor.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Estima a raiz quadrada por componente de um vetor.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Calcula a diferença de dois vetores.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Subtrai dois vetores que representam ângulos.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Calcula a soma horizontal dos componentes de um [**XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Arredoda cada componente de um vetor para o valor inteiro mais próximo na direção de zero.<br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de vetor da biblioteca DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
