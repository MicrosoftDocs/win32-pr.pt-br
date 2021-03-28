---
description: Para aplicar formatação especial ao texto, inicialize um objeto StringFormat e passe o endereço desse objeto para o método DrawString da classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formatar texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563243"
---
# <a name="formatting-text-gdi"></a>Formatar texto (GDI+)

Para aplicar formatação especial ao texto, inicialize um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e passe o endereço desse objeto para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Para desenhar texto formatado em um retângulo, você precisa de objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)e [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .

-   [Alinhando texto](#aligning-text)
-   [Configurando paradas de tabulação](#setting-tab-stops)
-   [Desenho de texto vertical](#drawing-vertical-text)

## <a name="aligning-text"></a>Alinhando texto

O exemplo a seguir desenha o texto em um retângulo. Cada linha de texto é centralizada (lado a lado) e todo o bloco de texto é centralizado (de cima para baixo) no retângulo.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



A ilustração a seguir mostra o retângulo e o texto centralizado.

![captura de tela de uma janela que contém um retângulo, que contém seis linhas de texto, centralizado horizontalmente](images/fontstext3.png)

O código anterior chama dois métodos do objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: setAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) e [**StringFormat:: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment). A chamada para **StringFormat:: setAlignment** especifica que cada linha de texto é centralizada no retângulo fornecido pelo terceiro argumento passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) . A chamada para **StringFormat:: SetLineAlignment** especifica que o bloco de texto é centralizado (de cima para baixo) no retângulo.

O valor [* * * * StringAlignmentCenter * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) é um elemento da enumeração **StringAlignment** , que é declarado em Gdiplusenums. h.

## <a name="setting-tab-stops"></a>Configurando paradas de tabulação

Você pode definir tabulações de tabulação para texto chamando o método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) de um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) e, em seguida, passando o endereço desse objeto **StringFormat** para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

O exemplo a seguir define as paradas de tabulação em 150, 250 e 350. Em seguida, o código exibe uma lista com guias de nomes e pontuações de teste.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



A ilustração a seguir mostra o texto com guias.

![ilustração de um retângulo que contém quatro colunas de texto; cada coluna é esquerda-alinhado](images/fontstext4.png)

O código anterior passa três argumentos para o método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) . O terceiro argumento é o endereço de uma matriz que contém os deslocamentos da guia. O segundo argumento indica que há três deslocamentos nessa matriz. O primeiro argumento passado para **StringFormat:: SetTabStops** é 0, o que indica que o primeiro deslocamento na matriz é medido da posição 0, a borda esquerda do retângulo delimitador.

## <a name="drawing-vertical-text"></a>Desenho de texto vertical

Você pode usar um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) para especificar que o texto seja desenhado verticalmente em vez de horizontalmente.

O exemplo a seguir passa o valor [* * * * StringFormatFlagsDirectionVertical * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) para o método [**StringFormat:: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) de um objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) . O endereço desse objeto **StringFormat** é passado para o método [drawstring](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O valor [* * * * StringFormatFlagsDirectionVertical * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) é um elemento da enumeração **StringFormatFlags** , que é declarado em Gdiplusenums. h.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



A ilustração a seguir mostra o texto vertical.

![ilustração mostrando uma janela que contém o texto girado 90 graus no sentido horário](images/fontstext5.png)

 

 



