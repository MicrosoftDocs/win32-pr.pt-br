---
description: Ao preencher uma forma, você deve passar o endereço de um objeto Brush para um dos métodos de preenchimento da classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Desenhando com pincéis opacos e semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce5bb89c460c9769f805fb33af9eb91e9d8207448e702476aff4d25dec33a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248870"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Desenhando com pincéis opacos e semitransparentes

Ao preencher uma forma, você deve passar o endereço de um objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) para um dos métodos de preenchimento da [**classe Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) O único parâmetro do construtor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) é um [**objeto**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) Color. Para preencher uma forma opaca, defina o componente alfa da cor como 255. Para preencher uma forma semitransparente, defina o componente alfa para qualquer valor de 1 a 254.

Ao preencher uma forma semitransparente, a cor da forma é combinada com as cores da tela de fundo. O componente alfa especifica como as cores da forma e da plano de fundo são misturadas; Os valores alfa próximos a 0 colocam mais peso nas cores da tela de fundo e os valores alfa próximos a 255 ponderam mais sobre a cor da forma.

O exemplo a seguir desenha uma imagem e, em seguida, preenche três re elipses que se sobrepõem à imagem. A primeira elipse usa um componente alfa de 255, portanto, é opaca. As segunda e terceira elipses usam um componente alfa de 128, para que sejam semitransparentes; É possível ver a imagem da tela de fundo pelas elipses. A chamada para [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) faz com que a combinação da terceira elipse seja feita em conjunto com a correção gama.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



A ilustração a seguir mostra a saída do código anterior.

![ilustração mostrando uma imagem sobreposição por três reellipses: uma opaca, uma ligeiramente transparente, uma muito transparente](images/compqualellipse.png)

 

 



