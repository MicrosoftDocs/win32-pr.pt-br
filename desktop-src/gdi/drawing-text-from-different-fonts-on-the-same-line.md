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
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="fafb5-103">Desenho de texto de fontes diferentes na mesma linha</span><span class="sxs-lookup"><span data-stu-id="fafb5-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="fafb5-104">Estilos de tipo diferentes dentro de uma família de fontes podem ter larguras diferentes.</span><span class="sxs-lookup"><span data-stu-id="fafb5-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="fafb5-105">Por exemplo, os estilos de negrito e itálico de uma família são sempre mais largos do que o estilo romano para um tamanho de ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="fafb5-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="fafb5-106">Ao exibir ou imprimir vários estilos de tipo em uma única linha, você deve manter o controle da largura da linha para evitar ter caracteres exibidos ou impressos em cima um do outro.</span><span class="sxs-lookup"><span data-stu-id="fafb5-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="fafb5-107">Você pode usar duas funções para recuperar a largura (ou extensão) do texto na fonte atual.</span><span class="sxs-lookup"><span data-stu-id="fafb5-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="fafb5-108">A função [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) computa a largura e a altura de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fafb5-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="fafb5-109">Se a cadeia contiver um ou mais caracteres de tabulação, a largura da cadeia de caracteres será baseada em uma matriz especificada de posições de tabulação.</span><span class="sxs-lookup"><span data-stu-id="fafb5-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="fafb5-110">A função [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) computa a largura e a altura de uma linha de texto.</span><span class="sxs-lookup"><span data-stu-id="fafb5-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="fafb5-111">Quando necessário, o sistema sintetiza uma fonte alterando os bitmaps de caractere.</span><span class="sxs-lookup"><span data-stu-id="fafb5-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="fafb5-112">Para sintetizar um caractere em negrito, o sistema desenha o caractere duas vezes: no ponto de partida e, novamente, um pixel à direita do ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="fafb5-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="fafb5-113">Para resumir um caractere em uma fonte em itálico, o sistema desenha duas linhas de pixels na parte inferior da célula de caracteres, move o ponto de partida um pixel para a direita, desenha as duas linhas seguintes e continua até que o caractere tenha sido desenhado.</span><span class="sxs-lookup"><span data-stu-id="fafb5-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="fafb5-114">Ao deslocar pixels, cada caractere parece ser distorcido à direita.</span><span class="sxs-lookup"><span data-stu-id="fafb5-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="fafb5-115">A quantidade de distorção é uma função da altura do caractere.</span><span class="sxs-lookup"><span data-stu-id="fafb5-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="fafb5-116">Uma maneira de escrever uma linha de texto que contenha várias fontes é usar a função [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) após cada chamada para [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) e adicionar o comprimento a uma posição atual.</span><span class="sxs-lookup"><span data-stu-id="fafb5-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="fafb5-117">O exemplo a seguir grava a linha "esta é uma cadeia de caracteres de exemplo."</span><span class="sxs-lookup"><span data-stu-id="fafb5-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="fafb5-118">usar caracteres em negrito para "Este é um", alterna para caracteres em itálico para "Sample" e, em seguida, retorna para caracteres em negrito para "String".</span><span class="sxs-lookup"><span data-stu-id="fafb5-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="fafb5-119">Depois de imprimir todas as cadeias de caracteres, ele restaura os personagens padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="fafb5-119">After printing all the strings, it restores the system default characters.</span></span>


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



<span data-ttu-id="fafb5-120">Neste exemplo, a função [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) Inicializa os membros de uma estrutura de [tamanho](/previous-versions//dd145106(v=vs.85)) com o comprimento e a altura da cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="fafb5-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="fafb5-121">A função [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera a folga da fonte atual.</span><span class="sxs-lookup"><span data-stu-id="fafb5-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="fafb5-122">Como o folga será zero se a fonte for uma fonte TrueType, o valor de folga não alterará o posicionamento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fafb5-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="fafb5-123">Para fontes de varredura, no entanto, é importante usar o valor de folga.</span><span class="sxs-lookup"><span data-stu-id="fafb5-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="fafb5-124">A folga é subtraída da cadeia de caracteres em negrito uma vez, para colocar os caracteres subsequentes próximos ao final da cadeia de caracteres se a fonte for uma fonte de varredura.</span><span class="sxs-lookup"><span data-stu-id="fafb5-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="fafb5-125">Como a folga afeta o início e o fim da cadeia de caracteres em itálico em uma fonte de rasterização, os glifos começam à direita do local especificado e terminam à esquerda do ponto de extremidade da última célula de caractere.</span><span class="sxs-lookup"><span data-stu-id="fafb5-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="fafb5-126">(A função [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera a extensão das células de caractere, não a extensão dos glifos.) Para considerar a folga na cadeia de caracteres em itálico rasterizada, o exemplo subtrai a folga antes de colocar a cadeia de caracteres e subtrai-a novamente antes de colocar os caracteres subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fafb5-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="fafb5-127">A função [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) adiciona espaço extra aos caracteres de quebra em uma linha de texto.</span><span class="sxs-lookup"><span data-stu-id="fafb5-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="fafb5-128">Você pode usar a função [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) para determinar a extensão de uma cadeia de caracteres e, em seguida, subtrair essa extensão da quantidade total de espaço que a linha deve ocupar e usar a função [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir o espaço extra entre os caracteres de quebra na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fafb5-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="fafb5-129">A função [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) adiciona espaço extra a cada célula de caractere na fonte selecionada, incluindo o caractere de quebra.</span><span class="sxs-lookup"><span data-stu-id="fafb5-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="fafb5-130">(Você pode usar a função [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) para determinar a quantidade atual de espaço extra que está sendo adicionada às células de caracteres; a configuração padrão é zero.)</span><span class="sxs-lookup"><span data-stu-id="fafb5-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="fafb5-131">Você pode inserir caracteres com maior precisão usando a função [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) ou [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) para recuperar as larguras de caracteres individuais em uma fonte.</span><span class="sxs-lookup"><span data-stu-id="fafb5-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="fafb5-132">A função [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) é mais precisa do que a função [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , mas só pode ser usada com fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="fafb5-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="fafb5-133">O espaçamento ABC também permite que um aplicativo execute um alinhamento de texto muito preciso.</span><span class="sxs-lookup"><span data-stu-id="fafb5-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="fafb5-134">Por exemplo, quando o direito do aplicativo alinha uma fonte Roman de rasterização sem usar o espaçamento ABC, a largura de avanço é calculada como a largura do caractere.</span><span class="sxs-lookup"><span data-stu-id="fafb5-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="fafb5-135">Isso significa que o espaço em branco à direita do glifo no bitmap está alinhado, não o glifo em si.</span><span class="sxs-lookup"><span data-stu-id="fafb5-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="fafb5-136">Usando larguras ABC, os aplicativos têm mais flexibilidade no posicionamento e na remoção de espaço em branco ao alinhar texto, pois eles têm informações que permitem que eles controlem de forma fina o espaçamento entre caracteres.</span><span class="sxs-lookup"><span data-stu-id="fafb5-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
