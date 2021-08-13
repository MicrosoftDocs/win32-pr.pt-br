---
description: O recorte envolve restringir o desenho a uma determinada região. A ilustração a seguir mostra a cadeia de caracteres &\# 0034; Hello&\# 0034; recortado para uma região em forma de coração.
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

O recorte envolve restringir o desenho a uma determinada região. A ilustração a seguir mostra a cadeia de caracteres "Hello" recortada em uma região em forma de coração.

![ilustração mostrando partes da cadeia de caracteres "hello" dentro de um coração vermelho](images/aboutgdip02-art30.png)

As regiões podem ser construídas de caminhos e os caminhos podem conter os contornos de cadeias de caracteres, para que você possa usar o texto descrito para recorte. A ilustração a seguir mostra um conjunto de re elipses concêntricas recortados no interior de uma cadeia de caracteres de texto.

![ilustração mostrando a cadeia de caracteres "hello" preenchida por um padrão de círculos concêntricos](images/aboutgdip02-art31.png)

Para desenhar com recorte, crie um objeto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) chame seu método [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) e, em seguida, chame os métodos de desenho do mesmo **objeto Graphics.** O exemplo a seguir desenha uma linha que é recortada para uma região retangular.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



A ilustração a seguir mostra a região retangular junto com a linha recortada.

![ilustração mostrando um retângulo com uma linha diagonal de cima para baixo](images/aboutgdip02-art31a.png)

 

 



