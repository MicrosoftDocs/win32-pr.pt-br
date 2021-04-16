---
description: Embora a largura e a densidade dos termos muitas vezes sejam usados informalmente, eles têm significados muito importantes e distintos diferentes. Como resultado, você deve entender os significados para cada um e como interpretar os valores que o Direct3D usa para descrevê-los.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Largura vs. pitch (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557272"
---
# <a name="width-vs-pitch-direct3d-9"></a>Largura vs. pitch (Direct3D 9)

Embora a largura e a densidade dos termos muitas vezes sejam usados informalmente, eles têm significados muito importantes e distintos diferentes. Como resultado, você deve entender os significados para cada um e como interpretar os valores que o Direct3D usa para descrevê-los.

O Direct3D usa a estrutura [**\_ desc D3DSURFACE**](d3dsurface-desc.md) para transportar informações que descrevem uma superfície. Entre outras coisas, essa estrutura é definida para conter informações sobre as dimensões de uma superfície, bem como sobre como essas dimensões são representadas na memória. A estrutura usa os membros de altura e largura para descrever as dimensões lógicas da superfície. Ambos os membros são medidos em pixels. Portanto, os valores de altura e largura de uma superfície de 640 x 480 são os mesmos, seja uma superfície de 8 bits ou uma superfície RGB de 24 bits.

Quando você bloqueia uma superfície usando o método [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , o método preenche uma estrutura [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) que contém a inclinação da superfície e um ponteiro para os bits bloqueados. O valor no membro pitch descreve a densidade da memória da superfície, também chamada de Stride. Pitch é a distância, em bytes, entre dois endereços de memória que representam o início de uma linha de bitmap e o início da próxima linha de bitmap. Como Pitch é medido em bytes em vez de pixels, uma superfície 640x480x8 tem um valor de densidade muito diferente de uma superfície com as mesmas dimensões, mas um formato de pixel diferente. Além disso, o valor de pitch às vezes reflete os bytes que o Direct3D reservou como um cache, portanto, não é seguro pressupor que a densidade é apenas a largura multiplicada pelo número de bytes por pixel. Em vez disso, visualize a diferença entre largura e densidade, conforme mostrado no diagrama a seguir.

![diagrama da densidade e largura do mesmo buffer frontal, buffer de fundo e cache](images/pitch.png)

Neste diagrama, o buffer frontal e o buffer de fundo são 640x480x8 e o cache é 384x480x8.

Ao acessar as superfícies diretamente, tome cuidado para permanecer dentro da memória alocada para as dimensões da superfície e fique fora de qualquer memória reservada para o cache. Além disso, ao bloquear apenas uma parte de uma superfície, você deve permanecer dentro do retângulo especificado ao bloquear a superfície. A falha ao seguir essas diretrizes terá resultados imprevisíveis. Ao renderizar diretamente na memória da superfície, sempre use a densidade retornada pelo método [**IDirect3DSurface9:: LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) . Não assuma um timbre baseado apenas no modo de exibição. Se seu aplicativo funcionar em alguns adaptadores de vídeo, mas parecer ilegível em outros, isso pode ser a causa do problema.

Para obter mais informações, consulte [acessando a memória da superfície diretamente (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
