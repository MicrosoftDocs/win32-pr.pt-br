---
description: Ao preencher uma forma, você deve passar o endereço de um objeto de pincel para um dos métodos Fill da classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Desenho com pincéis opacos e semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091471"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Desenho com pincéis opacos e semitransparentes

Ao preencher uma forma, você deve passar o endereço de um objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) para um dos métodos Fill da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O parâmetro One do construtor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) é um objeto [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) . Para preencher uma forma opaca, defina o componente alfa da cor como 255. Para preencher uma forma semitransparente, defina o componente alfa para qualquer valor de 1 a 254.

Ao preencher uma forma semitransparente, a cor da forma é combinada com as cores da tela de fundo. O componente alfa Especifica como as cores de forma e de plano de fundo são misturadas; os valores Alfa próximos 0 colocam mais peso nas cores do plano de fundo, e os valores Alfa próximos a 255 colocam mais importância na cor da forma.

O exemplo a seguir desenha uma imagem e, em seguida, preenche as três reticências que se sobrepõem à imagem. A primeira elipse usa um componente alfa de 255, portanto, é opaca. As segunda e terceira elipses usam um componente alfa de 128, para que sejam semitransparentes; É possível ver a imagem da tela de fundo pelas elipses. A chamada para [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) faz com que a combinação da terceira elipse seja feita em conjunto com a correção gama.


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

![ilustração mostrando uma imagem sobreposta por três elipses: uma opaca, uma levemente transparente, uma muito transparente](images/compqualellipse.png)

 

 



