---
description: Embora os termos largura e tom geralmente sejam usados informalmente, eles têm significados muito importantes e distintamente diferentes. Como resultado, você deve entender os significados de cada um e como interpretar os valores que o Direct3D usa para descrevê-los.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Largura versus Tom (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1c697ec4c9278a78a5539818b30038d99fc9d59d96af7f22ee87c33949abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095506"
---
# <a name="width-vs-pitch-direct3d-9"></a>Largura versus Tom (Direct3D 9)

Embora os termos largura e tom geralmente sejam usados informalmente, eles têm significados muito importantes e distintamente diferentes. Como resultado, você deve entender os significados de cada um e como interpretar os valores que o Direct3D usa para descrevê-los.

O Direct3D usa a [**estrutura D3DSURFACE \_ DESC**](d3dsurface-desc.md) para transportar informações que descrevem uma superfície. Entre outras coisas, essa estrutura é definida para conter informações sobre as dimensões de uma superfície, bem como como essas dimensões são representadas na memória. A estrutura usa os membros Height e Width para descrever as dimensões lógicas da superfície. Ambos os membros são medidos em pixels. Portanto, os valores de Altura e Largura para uma superfície de 640 x 480 são os mesmos, seja uma superfície de 8 bits ou uma superfície RGB de 24 bits.

Quando você bloquear uma superfície usando o método [**IDirect3DSurface9::LockRect,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) o método preenche uma estrutura [**D3DLOCKED \_ RECT**](d3dlocked-rect.md) que contém o tom da superfície e um ponteiro para os bits bloqueados. O valor no membro Pitch descreve o tom de memória da superfície, também chamado de stride. Pitch é a distância, em bytes, entre dois endereços de memória que representam o início de uma linha de bitmap e o início da próxima linha de bitmap. Como o tom é medido em bytes em vez de pixels, uma superfície 640x480x8 tem um valor de tom muito diferente de uma superfície com as mesmas dimensões, mas um formato de pixel diferente. Além disso, o valor de tom às vezes reflete bytes que o Direct3D reservou como um cache, portanto, não é seguro supor que o tom seja apenas a largura multiplicada pelo número de bytes por pixel. Em vez disso, visualize a diferença entre largura e tom, conforme mostrado no diagrama a seguir.

![diagrama de tom e largura para o mesmo buffer frontal, buffer de fundo e cache](images/pitch.png)

Neste diagrama, o buffer frontal e o buffer de fundo são 640x480x8 e o cache é 384x480x8.

Ao acessar superfícies diretamente, tome cuidado para permanecer dentro da memória alocada para as dimensões da superfície e ficar fora de qualquer memória reservada para cache. Além disso, quando você bloquear apenas uma parte de uma superfície, deverá permanecer dentro do retângulo especificado ao bloquear a superfície. Não seguir essas diretrizes terá resultados imprevisíveis. Ao renderizar diretamente na memória da superfície, sempre use o tom retornado pelo [**método IDirect3DSurface9::LockRect.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) Não suponha que uma apresentação seja baseada apenas no modo de exibição. Se o aplicativo funciona em alguns adaptadores de exibição, mas parece com outros, isso pode ser a causa do problema.

Para obter mais informações, [consulte Acessando diretamente a memória do Surface (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
