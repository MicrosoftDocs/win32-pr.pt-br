---
description: Ao desenhar uma linha, você deve passar o endereço de um objeto Caneta para o método DrawLine da classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Desenhar linhas opacas e semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14cdf31a80be9ac2a0cf61a2a8eb82f530dc3558c876cba9190a79f42ac35baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036754"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Desenhar linhas opacas e semitransparentes

Ao desenhar uma linha, você deve passar o endereço de um objeto [**Caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para o [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) da [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Um dos parâmetros do construtor **Caneta** é um [**objeto**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Color. Para desenhar uma linha opaca, defina o componente alfa da cor como 255. Para desenhar uma linha semitransparente, defina o componente alfa para qualquer valor de 1 a 254.

Ao desenhar uma linha semitransparente em uma tela de fundo, a cor da linha é combinada com as cores da tela de fundo. O componente alfa especifica como as cores da linha e da plano de fundo são misturadas; Os valores alfa próximos a 0 colocam mais peso nas cores da tela de fundo e os valores alfa próximos a 255 ponderam mais na cor da linha.

O exemplo a seguir desenha uma imagem e, em seguida, desenha três linhas que usam a imagem como uma plano de fundo. A primeira linha usa um componente alfa de 255, portanto, é opaca. As segunda e terceira linhas usam um componente alfa de 128, para que sejam semitransparentes. É possível ver a imagem da tela de fundo pelas linhas. A chamada para [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) faz com que a combinação da terceira linha seja feita em conjunto com a correção gama.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



A ilustração a seguir mostra a saída do código anterior.

![ilustração mostrando uma imagem sobreposição por três linhas largas: uma opaca, uma ligeiramente transparente e outra muito transparente](images/compqualline.png)

 

 



