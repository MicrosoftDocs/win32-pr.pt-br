---
description: Ao longo da programação Direct3D e Window, os objetos na tela são referidos em termos de retângulos delimitadores.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Retângulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087244"
---
# <a name="rectangles-direct3d-9"></a>Retângulos (Direct3D 9)

Ao longo da programação Direct3D e Window, os objetos na tela são referidos em termos de retângulos delimitadores. Os lados de um retângulo delimitador sempre são paralelos às laterais da tela, para que o retângulo possa ser descrito por dois pontos, o canto superior esquerdo e o canto inferior direito. A maioria dos aplicativos usa a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para transportar informações sobre um retângulo delimitador para uso durante a transferência para a tela ou para executar a detecção de clique.

Em C++, a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) tem a definição a seguir.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



No exemplo anterior, os membros esquerdo e superior são as coordenadas x e y do canto superior esquerdo do retângulo delimitador. Da mesma forma, os membros direito e inferior compõem as coordenadas do canto inferior direito. A ilustração a seguir mostra como você pode visualizar esses valores.

![ilustração do retângulo delimitado pelos valores esquerdo, superior, direito e inferior](images/rect.png)

A coluna de pixels na borda direita e a linha de pixels na borda inferior não estão incluídas no RECT. Por exemplo, bloquear um RECT com membros {10, 10, 138, 138} resulta em um objeto com 128 pixels em largura e altura.

No interesse da eficiência, da consistência e da facilidade de uso, todas as funções de apresentação do Direct3D funcionam com retângulos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenar sistemas e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
