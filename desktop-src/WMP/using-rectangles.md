---
title: usando retângulos (Windows Media Player SDK)
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
ms.openlocfilehash: 79dd46928ccf8f8a0a465fa71fbb6b1bc1b4f48cbdb5c37b4b93ffd21c78c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117290"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>usando retângulos (Windows Media Player SDK)

Os retângulos são usados para especificar áreas retangulares no Microsoft Windows. você pode criar vários retângulos em sua janela, mas Windows Media Player fornece os valores de um retângulo por meio da função [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) . Se o seu plug-in renderizar usando uma janela, o retângulo será a área do cliente da janela. isso é chamado de retângulo prc e define o retângulo para o qual Windows Media Player exibirá sua visualização. Use isso frequentemente para ter certeza de que você não desenha além das extensões do retângulo fornecido pelo Windows Media Player.

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

 

 




