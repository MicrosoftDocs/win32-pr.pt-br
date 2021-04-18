---
description: Lista as funções de matriz fornecidas pelo DirectXMath.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Funções de matriz da biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9c6110db6bb3ce9ee883406445ad3a04681cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786289"
---
# <a name="directxmath-library-matrix-functions"></a>Funções de matriz da biblioteca DirectXMath

Lista as funções de matriz fornecidas pelo DirectXMath.

> [!Note]  
> O DirectXMath oferece as versões da esquerda e da mão direita das funções de matriz com ' destroly ', mas sempre pressupõe um formato de linha principal.

 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Cria uma matriz de transformação afim.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Cria uma matriz de transformação afim 2D no plano XY. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Computa o determinante de uma matriz.<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Cria a matriz de identidade.<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Computa o inverso de uma matriz.<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Testa se uma matriz é a matriz de identidade.<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Testa se algum dos elementos de uma matriz é infinito positivo ou negativo.<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Testa se qualquer um dos elementos de uma matriz é NaN.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Cria uma matriz de exibição para um sistema de coordenadas de mão esquerda usando uma posição da câmera, um sentido para cima e um ponto focal.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Cria uma matriz de exibição para um sistema de coordenadas de mão direita usando uma posição da câmera, um sentido para cima e um ponto focal.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Cria uma matriz de exibição para um sistema de coordenadas de mão esquerda usando uma posição da câmera, um sentido para cima e uma direção da câmera.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Cria uma matriz de exibição para um sistema de coordenadas de mão direita usando uma posição da câmera, um sentido para cima e uma direção da câmera.<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Computa o produto de duas matrizes.<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Computa a transpoção do produto de duas matrizes.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Cria uma matriz de projeção ortogonal para um sistema de coordenadas de mão esquerda.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Cria uma matriz de projeção ortogonal personalizada para um sistema de coordenadas de mão esquerda.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Cria uma matriz de projeção ortogonal personalizada para um sistema de coordenadas de mão direita.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Cria uma matriz de projeção ortogonal para um sistema de coordenadas de mão direita.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Cria uma matriz de projeção de perspectiva à esquerda com base em um campo de visão.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Cria uma matriz de projeção de perspectiva à direita com base em um campo de visão.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Cria uma matriz de projeção de perspectiva à esquerda.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Cria uma versão personalizada de uma matriz de projeção de perspectiva à esquerda.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Cria uma versão personalizada de uma matriz de projeção de perspectiva à direita.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Cria uma matriz de projeção de perspectiva à direita.<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Cria uma matriz de transformação projetada para refletir vetores por meio de um determinado plano.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Cria uma matriz que gira em um eixo arbitrário.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Cria uma matriz que gira em um vetor normal arbitrário.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Cria uma matriz de rotação de um Quaternion.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Cria uma matriz de rotação com base em um determinado timbre, guinada e roll (ângulos de Euler).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Cria uma matriz de rotação com base em um vetor que contém os ângulos de Euler (Pitch, guinada e roll).<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Cria uma matriz que gira em volta do eixo x.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Cria uma matriz que gira em volta do eixo y.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Cria uma matriz que gira em volta do eixo z.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Cria uma matriz que é dimensionada ao longo do eixo x, eixo y e eixo z.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Cria uma matriz de dimensionamento de um vetor 3D.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Cria uma matriz com valores **float** .<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Cria uma matriz de transformação que achata a geometria em um plano.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Cria uma matriz de transformação.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Cria uma matriz de transformação 2D no plano XY.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Cria uma matriz de conversão a partir dos deslocamentos especificados.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Cria uma matriz de conversão de um vetor.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Computa a transpoção de uma matriz.<br/>                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de biblioteca DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
