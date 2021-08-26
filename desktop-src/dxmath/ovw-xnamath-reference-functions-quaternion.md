---
description: Lista as funções quaternion fornecidas pelo DirectXMath.
ms.assetid: 2d397c98-d0cd-08e0-6104-cca31bb6bd11
title: Funções de quatternion da Biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 333721cee48083156a8fc4ba31c6a716d837e431ed6d3a6dbb88958672a1c1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117536"
---
# <a name="directxmath-library-quaternion-functions"></a>Funções de quatternion da Biblioteca DirectXMath

Lista as funções quaternion fornecidas pelo DirectXMath.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                       | Descrição                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**XMQuaternionBaryCentric**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric)<br/>                                       | Retorna um ponto em coordenadas barycentric, usando os quaterões especificados.<br/>                         |
| [**XMQuaternionBaryCentricV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)<br/>                                     | Retorna um ponto em coordenadas barycentric, usando os quaterões especificados.<br/>                         |
| [**XMQuaternionConjugate**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)<br/>                                           | Calcula o conjugado de um quaterão.<br/>                                                              |
| [**XMQuaternionDot**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)<br/>                                                       | Calcula o produto de ponto de dois quaterões.<br/>                                                         |
| [**XMQuaternionEqual**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionequal)<br/>                                                   | Testa se dois quaterões são iguais.<br/>                                                             |
| [**XMQuaternionExp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)<br/>                                                       | Calcula o exponencial de um determinado quatternion puro.<br/>                                                 |
| [**XMQuaternionIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)<br/>                                             | Retorna o quatrion de identidade.<br/>                                                                     |
| [**XMQuaternionInverse**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)<br/>                                               | Calcula o inverso de um quaterão.<br/>                                                                |
| [**XMQuaternionIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)<br/>                                         | Testa se um quatternion específico é o quaterão de identidade.<br/>                                      |
| [**XMQuaternionIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisinfinite)<br/>                                         | Teste se qualquer componente de um quaterna é infinito positivo ou negativo.<br/>                  |
| [**XMQuaternionIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisnan)<br/>                                                   | Teste se qualquer componente de um quatern é um NaN.<br/>                                                 |
| [**XMQuaternionLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)<br/>                                                 | Calcula a magnitude de um quaterão.<br/>                                                              |
| [**XMQuaternionLengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)<br/>                                             | Calcula o quadrado da magnitude de um quaterão.<br/>                                                |
| [**XMQuaternionLn**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)<br/>                                                         | Calcula o logaritmo natural de um quaternion de unidade determinado.<br/>                                           |
| [**XMQuaternionMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)<br/>                                             | Calcula o produto de dois quaterões.<br/>                                                             |
| [**XMQuaternionNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize)<br/>                                           | Normaliza um quaterão.<br/>                                                                             |
| [**XMQuaternionNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)<br/>                                     | Estima a versão normalizada de um quaterão.<br/>                                                    |
| [**XMQuaternionNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnotequal)<br/>                                             | Testa se dois quaterões não são iguais.<br/>                                                         |
| [**XMQuaternionReciprocalLength**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionreciprocallength)<br/>                             | Calcula a recíproca da magnitude de um quaterna.<br/>                                            |
| [**XMQuaternionRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)<br/>                                     | Calcula um quatrion de rotação sobre um eixo.<br/>                                                        |
| [**XMQuaternionRotationMatrix**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)<br/>                                 | Calcula um quatrion de rotação de uma matriz de rotação.<br/>                                               |
| [**XMQuaternionRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationnormal)<br/>                                 | Calcula o quatrion de rotação sobre um vetor normal.<br/>                                              |
| [**XMQuaternionRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw)<br/>                     | Calcula um quatrion de rotação com base no tom, no yaw e no roll (ângulos de Euler).<br/>                     |
| [**XMQuaternionRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyawfromvector)<br/> | Calcula um quatrion de rotação com base em um vetor que contém os ângulos de Euler (tom, yaw e roll).<br/> |
| [**XMQuaternionSlerp**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp)<br/>                                                   | Interpola entre dois quatrões de unidade, usando interpolação linear esférica.<br/>                     |
| [**XMQuaternionSlerpV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)<br/>                                                 | Interpola entre dois quatrões de unidade, usando interpolação linear esférica.<br/>                     |
| [**XMQuaternionSquad**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad)<br/>                                                   | Interpola entre quatro quatrões de unidade, usando interpolação quadrática esférica.<br/>                |
| [**XMQuaternionSquadSetup**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)<br/>                                         | Fornece endereços de pontos de controle de instalação para interpolação quadrática esférica.<br/>                   |
| [**XMQuaternionSquadV**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)<br/>                                                 | Interpola entre quatro quatrões de unidade, usando interpolação quadrática esférica.<br/>                |
| [**XMQuaternionToAxisAngle**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)<br/>                                       | Calcula um eixo e um ângulo de rotação sobre esse eixo para um determinado quatternion.<br/>                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções da biblioteca DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
