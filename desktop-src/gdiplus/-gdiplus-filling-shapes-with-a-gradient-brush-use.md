---
description: Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Preenchendo formas com um pincel de gradiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988876"
---
# <a name="filling-shapes-with-a-gradient-brush"></a>Preenchendo formas com um pincel de gradiente

Você pode usar um pincel de gradiente para preencher uma forma com uma cor que muda gradualmente. Por exemplo, é possível usar um gradiente horizontal para preencher uma forma com uma cor que muda gradualmente à medida que você move da borda esquerda da forma para a borda direita. Imagine um retângulo com uma borda esquerda preta (representada pelos componentes vermelho, verde e azul 0, 0, 0) e uma borda direita vermelha (representada por 255, 0, 0). Se o retângulo tem 256 pixels de largura, o componente vermelho de um determinado pixel será maior do que o componente vermelho do pixel à esquerda. O pixel mais à esquerda em uma linha tem componentes de cor (0, 0, 0), o segundo pixel tem (1, 0, 0), o terceiro pixel tem (2, 0, 0) e assim por diante, até chegar ao pixel mais à direita, que tem componentes de cor (255, 0, 0). Esses valores de cor interpolados compõem o gradiente de cores.

Um gradiente linear muda de cor ao mover na horizontal, vertical ou em paralelo para uma linha inclinada especificada. Um gradiente de demarcador muda de cor ao mover sobre o interior e o limite de um demarcador. É possível personalizar gradientes de demarcador para obter uma grande variedade de efeitos.

O GDI+ fornece as classes [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) e [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , ambas herdadas da classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

Os tópicos a seguir abordam gradientes lineares e de caminho mais detalhadamente:

-   [Criando um gradiente linear](-gdiplus-creating-a-linear-gradient-use.md)
-   [Criando um gradiente de caminho](-gdiplus-creating-a-path-gradient-use.md)
-   [Aplicando a correção gama a um gradiente](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



