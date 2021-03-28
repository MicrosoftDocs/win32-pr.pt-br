---
description: Estilos de tipo diferentes dentro de uma família de fontes podem ter larguras diferentes.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Desenho de texto de fontes diferentes na mesma linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165082"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Desenho de texto de fontes diferentes na mesma linha

Estilos de tipo diferentes dentro de uma família de fontes podem ter larguras diferentes. Por exemplo, os estilos de negrito e itálico de uma família são sempre mais largos do que o estilo romano para um tamanho de ponto especificado. Ao exibir ou imprimir vários estilos de tipo em uma única linha, você deve manter o controle da largura da linha para evitar ter caracteres exibidos ou impressos em cima um do outro.

Você pode usar duas funções para recuperar a largura (ou extensão) do texto na fonte atual. A função [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) computa a largura e a altura de uma cadeia de caracteres. Se a cadeia contiver um ou mais caracteres de tabulação, a largura da cadeia de caracteres será baseada em uma matriz especificada de posições de tabulação. A função [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) computa a largura e a altura de uma linha de texto.

Quando necessário, o sistema sintetiza uma fonte alterando os bitmaps de caractere. Para sintetizar um caractere em negrito, o sistema desenha o caractere duas vezes: no ponto de partida e, novamente, um pixel à direita do ponto de partida. Para resumir um caractere em uma fonte em itálico, o sistema desenha duas linhas de pixels na parte inferior da célula de caracteres, move o ponto de partida um pixel para a direita, desenha as duas linhas seguintes e continua até que o caractere tenha sido desenhado. Ao deslocar pixels, cada caractere parece ser distorcido à direita. A quantidade de distorção é uma função da altura do caractere.

Uma maneira de escrever uma linha de texto que contenha várias fontes é usar a função [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) após cada chamada para [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) e adicionar o comprimento a uma posição atual. O exemplo a seguir grava a linha "esta é uma cadeia de caracteres de exemplo." usar caracteres em negrito para "Este é um", alterna para caracteres em itálico para "Sample" e, em seguida, retorna para caracteres em negrito para "String". Depois de imprimir todas as cadeias de caracteres, ele restaura os personagens padrão do sistema.


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



Neste exemplo, a função [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) Inicializa os membros de uma estrutura de [tamanho](/previous-versions//dd145106(v=vs.85)) com o comprimento e a altura da cadeia de caracteres especificada. A função [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera a folga da fonte atual. Como o folga será zero se a fonte for uma fonte TrueType, o valor de folga não alterará o posicionamento da cadeia de caracteres. Para fontes de varredura, no entanto, é importante usar o valor de folga.

A folga é subtraída da cadeia de caracteres em negrito uma vez, para colocar os caracteres subsequentes próximos ao final da cadeia de caracteres se a fonte for uma fonte de varredura. Como a folga afeta o início e o fim da cadeia de caracteres em itálico em uma fonte de rasterização, os glifos começam à direita do local especificado e terminam à esquerda do ponto de extremidade da última célula de caractere. (A função [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera a extensão das células de caractere, não a extensão dos glifos.) Para considerar a folga na cadeia de caracteres em itálico rasterizada, o exemplo subtrai a folga antes de colocar a cadeia de caracteres e subtrai-a novamente antes de colocar os caracteres subsequentes.

A função [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) adiciona espaço extra aos caracteres de quebra em uma linha de texto. Você pode usar a função [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) para determinar a extensão de uma cadeia de caracteres e, em seguida, subtrair essa extensão da quantidade total de espaço que a linha deve ocupar e usar a função [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir o espaço extra entre os caracteres de quebra na cadeia de caracteres. A função [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) adiciona espaço extra a cada célula de caractere na fonte selecionada, incluindo o caractere de quebra. (Você pode usar a função [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) para determinar a quantidade atual de espaço extra que está sendo adicionada às células de caracteres; a configuração padrão é zero.)

Você pode inserir caracteres com maior precisão usando a função [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) ou [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) para recuperar as larguras de caracteres individuais em uma fonte. A função [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) é mais precisa do que a função [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , mas só pode ser usada com fontes TrueType.

O espaçamento ABC também permite que um aplicativo execute um alinhamento de texto muito preciso. Por exemplo, quando o direito do aplicativo alinha uma fonte Roman de rasterização sem usar o espaçamento ABC, a largura de avanço é calculada como a largura do caractere. Isso significa que o espaço em branco à direita do glifo no bitmap está alinhado, não o glifo em si. Usando larguras ABC, os aplicativos têm mais flexibilidade no posicionamento e na remoção de espaço em branco ao alinhar texto, pois eles têm informações que permitem que eles controlem de forma fina o espaçamento entre caracteres.

 

 
