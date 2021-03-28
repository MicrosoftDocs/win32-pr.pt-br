---
description: Você pode usar o método DrawString da classe Graphics para desenhar texto em um local especificado ou dentro de um retângulo especificado.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Desenhar texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091470"
---
# <a name="drawing-text-gdi"></a>Desenhar texto (GDI+)

Você pode usar o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar texto em um local especificado ou dentro de um retângulo especificado.

-   [Texto de desenho em um local especificado](#drawing-text-at-a-specified-location)
-   [Desenhar texto em um retângulo](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Texto de desenho em um local especificado

Para desenhar texto em um local especificado, você precisa de objetos [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

O exemplo a seguir desenha a cadeia de caracteres "Olá" no local (30, 10). A família de fontes é Times New Roman. A fonte, que é um membro individual da família de fontes, é Times New Roman, tamanho 24 pixels, estilo regular. Suponha que **gráficos** seja um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

A ilustração a seguir mostra a saída do código anterior.

![captura de tela de uma pequena janela que contém o texto "Olá"](images/fontstext1.png)

No exemplo anterior, o construtor [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recebe uma cadeia de caracteres que identifica a família de fontes. O endereço do objeto **FontFamily** é passado como o primeiro argumento para o construtor [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . O segundo argumento passado para o construtor **Font** especifica o tamanho da fonte medida em unidades fornecidas pelo quarto argumento. O terceiro argumento especifica o estilo (regular, negrito, itálico e assim por diante) da fonte.

O método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) recebe cinco argumentos. O primeiro argumento é a cadeia de caracteres a ser desenhada, e o segundo argumento é o comprimento (em caracteres, não bytes) dessa cadeia de caracteres. Se a cadeia de caracteres for terminada em nulo, você poderá passar – 1 para o comprimento. O terceiro argumento é o endereço do objeto de [**fonte**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) que foi construído anteriormente. O quarto argumento é um objeto [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) que contém as coordenadas do canto superior esquerdo da cadeia de caracteres. O quinto argumento é o endereço de um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) que será usado para preencher os caracteres da cadeia de caracteres.

## <a name="drawing-text-in-a-rectangle"></a>Desenhar texto em um retângulo

Um dos métodos [**drawstring**](https://www.bing.com/search?q=**DrawString**) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tem um parâmetro *RectF* . Chamando esse método **drawstring** , você pode desenhar o texto que encapsula um retângulo especificado. Para desenhar texto em um retângulo, você precisa de objetos **gráficos**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)e [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

O exemplo a seguir cria um retângulo com o canto superior esquerdo (30, 10), largura 100 e altura 122. Em seguida, o código desenha uma cadeia de caracteres dentro desse retângulo. A cadeia de caracteres é restrita ao retângulo e encapsulada de forma que palavras individuais não sejam quebradas.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

A ilustração a seguir mostra o texto desenhado no retângulo.

![captura de tela de uma pequena janela contendo um recangle, dentro do qual aparece a primeira parte de uma sentença](images/fontstext2.png)

No exemplo anterior, o quarto argumento passado para o método [**drawstring**](https://www.bing.com/search?q=**DrawString**) é um objeto [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) que especifica o retângulo delimitador para o texto. O quinto parâmetro é do tipo [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— o argumento é **nulo** porque nenhuma formatação de cadeia de caracteres especial é necessária.
