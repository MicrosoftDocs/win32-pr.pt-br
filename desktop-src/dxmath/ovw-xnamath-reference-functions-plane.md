---
description: Lista as funções de plano fornecidas pelo DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funções de plano de biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a91e58ddad68c31bcc5579b2727891fdddd5b6737761c89d9db70ca21c56bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841196"
---
# <a name="directxmath-library-plane-functions"></a>Funções de plano de biblioteca DirectXMath

Lista as funções de plano fornecidas pelo DirectXMath.

Essas funções usam um XMVECTOR 4-vector para representar os coeficientes da equação de plano, ax + by + cz + D = 0, em que o componente X é um, o componente Y é B, o Z-Component é C e o W-Component é D.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                               | Descrição                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Calcula o produto de ponto entre um plano de entrada e um vetor 4D.<br/>                                    |
| [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Calcula o produto de ponto entre um plano de entrada e um vetor 3D.<br/>                                    |
| [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Calcula o produto de ponto entre o vetor normal de um plano e um vetor 3D.<br/>                      |
| [**XMPlaneEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Determina se dois planos são iguais.<br/>                                                                   |
| [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Computa a equação de um plano construído a partir de um ponto no plano e um vetor normal.<br/>           |
| [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Computa a equação de um plano construído a partir de três pontos no plano.<br/>                          |
| [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Localiza a interseção entre um plano e uma linha.<br/>                                                    |
| [**XMPlaneIntersectPlane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Localiza a interseção de dois planos.<br/>                                                                 |
| [**XMPlaneIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Testa se algum dos coeficientes de um plano é infinito positivo ou negativo.<br/>                    |
| [**XMPlaneIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Testa se qualquer um dos coeficientes de um plano é um NaN.<br/>                                            |
| [**XMPlaneNearEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Determina se dois planos são quase iguais.<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Normaliza os coeficientes de um plano para que os coeficientes de x, y e z formarem um vetor normal de unidade.<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Estima os coeficientes de um plano para que os coeficientes de x, y e z formarem um vetor normal de unidade.<br/>  |
| [**XMPlaneNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Determina se dois planos são desiguais.<br/>                                                                 |
| [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Transforma um plano por uma determinada matriz.<br/>                                                                 |
| [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Transforma um fluxo de planos por uma determinada matriz.<br/>                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de biblioteca DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
