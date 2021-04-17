---
title: Usando retângulos (SDK do Windows Media Player)
description: Usando retângulos
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizações, retângulos
- visualizações personalizadas, retângulos
- visualizações, função render
- visualizações personalizadas, função render
- Processar função, retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105791475"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Usando retângulos (SDK do Windows Media Player)

Os retângulos são usados para especificar áreas retangulares no Microsoft Windows. Você pode criar vários retângulos em sua janela, mas o Windows Media Player fornece os valores de um retângulo por meio da função [IWMPEffects:: render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) . Se o seu plug-in renderizar usando uma janela, o retângulo será a área do cliente da janela. Isso é chamado de retângulo PRC e define o retângulo pelo qual o Windows Media Player exibirá sua visualização. Use isso frequentemente para ter certeza de que você não desenha além das extensões do retângulo fornecido pelo Windows Media Player.

Um retângulo tem quatro valores que o definem. Elas são esquerda, superior, direita e inferior. O canto superior esquerdo do retângulo é definido pela esquerda e na parte superior, e o canto inferior direito do retângulo é definido pela parte inferior e direita.

Use o código a seguir para obter as extensões do seu retângulo de desenho. Você precisa fazer isso porque o usuário pode redimensionar a janela e você deseja ter certeza de que está sempre desenhando em uma área que o usuário pode ver.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Por exemplo, para desenhar da esquerda para a direita, ao longo da parte superior da janela, use um código como este:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando renderização**](implementing-render.md)
</dt> </dl>

 

 




