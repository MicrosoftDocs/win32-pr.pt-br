---
description: O recorte envolve restringir o desenho a uma determinada região. A ilustração a seguir mostra a cadeia de caracteres &\# 0034; Olá&\# 0034; recortado em uma região em formato de coração.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Recorte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57534c5934270374af356956285ad13838630666795d9f06a2623cbd3b453ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067630"
---
# <a name="clipping-gdi"></a>Recorte (GDI+)

O recorte envolve restringir o desenho a uma determinada região. A ilustração a seguir mostra a cadeia de caracteres "Olá" recortada para uma região em formato de coração.

![ilustração mostrando partes da cadeia de caracteres "Olá" em um coração vermelho](images/aboutgdip02-art30.png)

As regiões podem ser construídas a partir de caminhos, e os caminhos podem conter os contornos das cadeias de caracteres, para que você possa usar texto com contorno para recorte. A ilustração a seguir mostra um conjunto de elipses concêntricas recortados para o interior de uma cadeia de caracteres de texto.

![ilustração mostrando a cadeia de caracteres "Olá" preenchida por um padrão de círculos concêntricos](images/aboutgdip02-art31.png)

Para desenhar com recorte, crie um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , chame seu método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) e, em seguida, chame os métodos de desenho desse mesmo objeto **gráfico** . O exemplo a seguir desenha uma linha recortada em uma região retangular.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



A ilustração a seguir mostra a região retangular junto com a linha recortada.

![ilustração mostrando um retângulo com uma linha diagonal de cima para baixo](images/aboutgdip02-art31a.png)

 

 



