---
description: Os vértices no espaço da câmera são calculados transformando os vértices de objeto com a matriz de visualização do mundo.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformações de espaço da câmera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089238"
---
# <a name="camera-space-transformations-direct3d-9"></a>Transformações de espaço da câmera (Direct3D 9)

Os vértices no espaço da câmera são calculados transformando os vértices de objeto com a matriz de visualização do mundo.

V = V \* wvMatrix

As normais de vértice, no espaço da câmera, são calculadas transformando as normais de objeto com a transposição inversa da matriz de exibição do mundo. A matriz de visualização do mundo poderá ou não ser ortogonal.

N = N \* (wvMatrix ⁻ ¹)<sup>T</sup>

A inversão de matrizes e a transposição de matrizes operam em uma matriz de 4 x 4. A multiplicação combina a normal com a parte 3 x 3 da matriz 4 x 4 resultante.

Se o estado de renderização, D3DRENDERSTATE \_ NORMALIZENORMALS for definido como **true**, os vetores normais de vértice serão normalizados após a transformação para o espaço da câmera da seguinte maneira:

N = norm(N)

A posição da luz no espaço da câmera é calculada transformando a posição da fonte de luz com a matriz de visualização.

LP = LP \* vMatrix

A direção para a luz no espaço da câmera para uma luz direcional é calculada multiplicando a direção da fonte de luz pela matriz de visualização, normalizando e anulando o resultado.

L<sub>dir</sub> =-normal (L<sub>dir</sub> \* wvMatrix)

Para o \_ ponto D3DLIGHT e D3DLIGHT \_ , a direção para Light é calculada da seguinte maneira:

L<sub>dir</sub> = normal (V \* LP), em que os parâmetros são definidos na tabela a seguir.



| Parâmetro       | Valor padrão | Tipo      | Descrição                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| F<sub>dir</sub> | N/D           | D3DVECTOR | Vetor de direção do vértice de objeto à luz          |
| V               | N/D           | D3DVECTOR | Posição do vértice no espaço da câmera                           |
| wvMatrix        | Identidade      | D3DMATRIX | Matriz composta contendo as transformções de modo de exibição e mundo |
| N               | N/D           | D3DVECTOR | Normal de vértice                                             |
| Lₚ              | N/D           | D3DVECTOR | Posição da luz no espaço da câmera                            |
| vMatrix         | Identidade      | D3DMATRIX | Matriz que contém a transformação de modo de exibição                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Matemática de iluminação](mathematics-of-lighting.md)
</dt> </dl>

 

 



