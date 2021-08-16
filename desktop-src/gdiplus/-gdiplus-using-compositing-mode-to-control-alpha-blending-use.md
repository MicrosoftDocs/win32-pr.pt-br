---
description: 'Pode haver ocasiões em que você deseja criar um bitmap fora da tela que tem as seguintes características:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Usando o modo de composição para controlar a combinação alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea2fc9d5be10e3a73bacf7f5a6dc5cbecb8c2992ac8cd961701f55fc2cb524d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611977"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Usando o modo de composição para controlar a combinação alfa

Pode haver ocasiões em que você deseja criar um bitmap fora da tela que tem as seguintes características:

-   Cores com valores alfabéticos inferiores a 255.
-   As cores não têm combinação alfa umas com as outras ao criar o bitmap.
-   Ao exibir o bitmap terminado, as cores no bitmap são combinadas em alfo com as cores da tela de fundo no dispositivo de vídeo.

Para criar um bitmap desse tipo, construa um objeto [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) em branco e, em seguida, construa um [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base nesse bitmap. De definir o modo de composição do **objeto Graphics** como CompositingModeSourceCopy.

O exemplo a seguir cria [**um objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um [**objeto Bitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) O código usa o **objeto Graphics** junto com dois pincéis semitransparentes (alfa = 160) para pintar no bitmap. O código preenche uma elipse vermelha e uma elipse verde usando os pincéis semitransparentes. A elipse verde sobrepõe a elipse vermelha, mas o verde não é mesclado com o vermelho porque o modo de composição do objeto **Graphics** está definido como CompositingModeSourceCopy.

Em seguida, o código se prepara para desenhar na tela chamando [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) e criando um [**objeto Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) com base em um contexto de dispositivo. O código desenha o bitmap na tela duas vezes: uma vez em uma tela de fundo branca e uma vez em uma tela de fundo multicolorida. Os pixels no bitmap que fazem parte das duas elipses têm um componente alfa de 160, de forma que as elipses são mescladas com as cores da tela de fundo na tela.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



A ilustração a seguir mostra a saída do código anterior. Observe que as elipses são mescladas com a tela de fundo, mas elas não são mescladas uma com a outra.

![ilustração mostrando duas reellipses de cores diferentes, cada uma delas combinando-se com seu plano de fundo multicolorido](images/sourcecopy.png)

O exemplo de código anterior tem a seguinte instrução:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Se desejar que as elipses sejam mescladas entre si e com a tela de fundo, altere essa instrução para o seguinte:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



A ilustração a seguir mostra a saída do código revisado.

![usando o modo de composição para controlar a ilustração de mesclagem alfa](images/sourceover.png)

 

 



