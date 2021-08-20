---
description: o tópico desenhando uma linha mostra como escrever um aplicativo Windows que usa Windows GDI+ para desenhar uma linha.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Desenhar uma cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9f9384631a0f3505e0bfd20a5e9b23ef3969432cd4ec82737ecf6f962062ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067499"
---
# <a name="drawing-a-string"></a>Desenhar uma cadeia de caracteres

o tópico [desenhando uma linha](-gdiplus-drawing-a-line-use.md) mostra como escrever um aplicativo Windows que usa Windows GDI+ para desenhar uma linha. Para desenhar uma cadeia de caracteres, substitua a função **OnPaint** mostrada no tópico pela seguinte função **OnPaint** :


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



o código anterior cria vários objetos GDI+. O objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fornece o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , que faz o desenho real. O objeto [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) especifica a cor da cadeia de caracteres.

O construtor [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recebe um único argumento de cadeia de caracteres que identifica a família de fontes. O endereço do objeto **FontFamily** é o primeiro argumento passado para o construtor [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . O segundo argumento passado para o construtor de [fonte](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) especifica o tamanho da fonte e o terceiro argumento especifica o estilo. O valor **FontStyleRegular** é um membro da enumeração [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que é declarado em Gdiplusenums. h. O último argumento para o construtor de **fonte** indica que o tamanho da fonte (24, nesse caso) é medido em pixels. O valor **UnitPixel** é um membro da enumeração de [**unidade**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .

O primeiro argumento passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) é o endereço de uma cadeia de caracteres largos. O segundo argumento, – 1, especifica que a cadeia de caracteres é terminada em nulo. (Se a cadeia de caracteres não for terminada em nulo, o segundo argumento deverá especificar o número de caracteres largos na cadeia de caracteres.) O terceiro argumento é o endereço do objeto [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . O quarto argumento é uma referência a um objeto [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) que especifica o local onde a cadeia de caracteres será desenhada. O último argumento é o endereço do objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , que especifica a cor da cadeia de caracteres.

 

 
