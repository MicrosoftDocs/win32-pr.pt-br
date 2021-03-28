---
description: Em alguns casos, um aplicativo deve ser capaz de enumerar as fontes disponíveis e selecionar a mais apropriada para uma determinada operação.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerando as fontes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165080"
---
# <a name="enumerating-the-installed-fonts"></a>Enumerando as fontes instaladas

Em alguns casos, um aplicativo deve ser capaz de enumerar as fontes disponíveis e selecionar a mais apropriada para uma determinada operação. Um aplicativo pode enumerar as fontes disponíveis chamando a função [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) ou [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) . Essas funções enviam informações sobre as fontes disponíveis para uma função de retorno de chamada que o aplicativo fornece. A função de retorno de chamada recebe informações em estruturas [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) e [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . (A estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contém informações sobre uma fonte TrueType. Quando a função de retorno de chamada recebe informações sobre uma fonte não-TrueType, as informações estão contidas em uma estrutura [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) Usando essas informações, um aplicativo pode limitar as opções do usuário somente às fontes disponíveis.

A função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) é semelhante à função [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , mas inclui alguma funcionalidade extra. O **EnumFontFamilies** permite que um aplicativo aproveite os estilos disponíveis com fontes TrueType. Aplicativos novos e atualizados devem usar **EnumFontFamilies** em vez de **EnumFonts**.

As fontes TrueType são organizadas em um nome de tipo de letra (por exemplo, Courier New) e nomes de estilo (por exemplo, itálico, negrito e negrito extra). A função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera todos os estilos associados a um nome de família especificado, e não apenas aos atributos Bold e italic. Por exemplo, quando o sistema inclui uma fonte TrueType chamada Courier New Extra-Bold, **EnumFontFamilies** a lista com as outras fontes do Courier New. Os recursos do **EnumFontFamilies** são úteis para fontes com estilos muitos ou incomuns e para fontes que cruzam bordas internacionais.

Se um aplicativo não fornecer um nome de tipo, as funções [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) fornecerão informações sobre uma fonte em cada família disponível. Para enumerar todas as fontes em um contexto de dispositivo, o aplicativo pode especificar **NULL** para o nome de tipo, compilar uma lista de tipos disponíveis e, em seguida, enumerar cada fonte em cada tipo.

O exemplo a seguir usa a função [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) para recuperar o número de famílias de fontes rasterizadas, vetoriais e TrueType disponíveis.


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



Este exemplo usa duas máscaras, RASTER \_ FontType e TrueType \_ FontType, para determinar o tipo de fonte que está sendo enumerada. Se o \_ bit FontType de rasterização for definido, a fonte será uma fonte de rasterização. Se o \_ bit FontType TrueType for definido, a fonte será uma fonte TrueType. Se nenhum bit for definido, a fonte será uma fonte vetorial. Uma terceira máscara, \_ FontType de dispositivo, é definida quando um dispositivo (por exemplo, uma impressora laser) dá suporte ao download de fontes TrueType; será zero se o dispositivo for um adaptador de vídeo, uma impressora matricial ou outro dispositivo de varredura. Um aplicativo também pode usar a \_ máscara FontType do dispositivo para distinguir fontes de varredura fornecidas pela GDI das fontes fornecidas pelo dispositivo. O sistema pode simular atributos em negrito, itálico, sublinhado e riscado para fontes de varredura fornecidas pela GDI, mas não para fontes fornecidas pelo dispositivo.

Um aplicativo também pode verificar bits 1 e 2 no membro **tmPitchAndFamily** da estrutura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para identificar uma fonte TrueType. Se o bit 1 for 0 e o bit 2 for 1, a fonte será uma fonte TrueType.

As fontes de vetor são categorizadas como conjunto \_ de caracteres OEM em vez de \_ charset ANSI. Alguns aplicativos identificam fontes de vetor usando essas informações, verificando o membro **tmCharSet** da estrutura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) . Essa categorização geralmente impede que o mapeador de fontes escolha fontes vetoriais, a menos que elas sejam especificamente solicitadas. (A maioria dos aplicativos não usa mais fontes vetoriais porque seus traços são linhas únicas e demoram mais para serem desenhados do que as fontes TrueType, que oferecem muitos dos mesmos recursos de dimensionamento e rotação que exigiam fontes vetoriais.)

 

 
