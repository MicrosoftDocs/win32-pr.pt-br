---
description: As funções a seguir são usadas com fontes e texto.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Funções de fonte e texto (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a4dd6f000356dfb0e52c34fadef81bd6e8843e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502422"
---
# <a name="font-and-text-functions-windows-gdi"></a>Funções de fonte e texto (GDI do Windows)

As funções a seguir são usadas com fontes e texto.



| Função                                                   | Descrição                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AddFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Adiciona uma fonte inserida à tabela de fontes do sistema.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Adiciona um recurso de fonte à tabela de fontes do sistema.                                                                       |
| [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Adiciona uma fonte privada ou não enumerável à tabela de fontes do sistema.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Cria uma fonte lógica.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Cria uma fonte lógica a partir de uma estrutura.                                                                             |
| [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Cria uma fonte lógica a partir de uma estrutura.                                                                             |
| [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Desenha texto formatado em um retângulo.                                                                                 |
| [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Desenha texto formatado em Rectangle.                                                                                   |
| [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))             | Uma função de aplicativo definedcallback usada com [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) para processar fontes. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Enumera todas as fontes no sistema com determinadas características.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Desenha uma cadeia de caracteres.                                                                                            |
| [**GetAspectRatioFilterEx**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Obtém a configuração para o filtro de taxa de proporção.                                                                        |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Obtém as larguras de caracteres consecutivos da fonte TrueType.                                                    |
| [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Obtém as larguras de caracteres consecutivos da fonte atual.                                                     |
| [**GetCharABCWidthsI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Obtém as larguras de índices de glifos consecutivos ou de uma matriz de índices de glifos da fonte TrueType.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Obtém informações sobre uma cadeia de caracteres.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Obtém as larguras de caracteres consecutivos da fonte atual.                                                     |
| [**GetCharWidthFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Obtém as larguras fracionárias de caracteres consecutivos da fonte atual.                                          |
| [**GetCharWidthI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Obtém as larguras de índices de glifos consecutivos ou uma matriz de índices de glifo da fonte atual.                     |
| [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Obtém dados de métrica para uma fonte TrueType.                                                                                |
| [**GetFontLanguageInfo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Retorna informações sobre a fonte selecionada para um contexto de exibição.                                                   |
| [**GetFontUnicodeRanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Informa quais caracteres Unicode têm suporte em uma fonte.                                                              |
| [**GetGlyphIndices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Traduz uma cadeia de caracteres em uma matriz de índices de glifos.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Obtém a estrutura de tópicos ou o bitmap de um caractere na fonte TrueType.                                                     |
| [**GetKerningPairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Obtém os pares de kerning de caracteres para uma fonte.                                                                         |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Obtém métricas de texto para fontes TrueType.                                                                                |
| [**GetRasterizerCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Informa se as fontes TrueType estão instaladas.                                                                          |
| [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Computa a largura e a altura de uma cadeia de caracteres, incluindo tabulações.                                                 |
| [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Obtém a configuração de alinhamento de texto para um contexto de dispositivo.                                                                |
| [**GetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Obtém o espaçamento entre caracteres atual para um contexto de dispositivo.                                                        |
| [**GetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Obtém a cor do texto de um contexto de dispositivo.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Obtém o número de caracteres em uma cadeia de caracteres que se ajustará dentro de um espaço.                                              |
| [**GetTextExtentExPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Obtém o número de índices de glifo que se ajustarão em um espaço.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Computa a largura e a altura de uma cadeia de caracteres de texto.                                                                   |
| [**GetTextExtentPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Computa a largura e a altura de uma matriz de índices de glifos.                                                          |
| [**GetTextFace**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Obtém o nome da fonte selecionada em um contexto de dispositivo.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Preenche um buffer com as métricas de uma fonte.                                                                          |
| [**Semitextoout**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Desenha várias cadeias de caracteres usando as cores de fonte e de texto em um contexto de dispositivo.                                            |
| [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Remove uma fonte cuja fonte foi inserida em um documento da tabela de fontes do sistema.                                   |
| [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Remove as fontes de um arquivo da tabela de fontes do sistema.                                                              |
| [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Remove uma fonte privada ou não enumerável da tabela de fontes do sistema.                                                 |
| [**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Altera o algoritmo usado para mapear fontes lógicas para fontes físicas.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Define os sinalizadores de alinhamento de texto para um contexto de dispositivo.                                                                  |
| [**SetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Define o espaçamento entre caracteres.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Define a cor do texto para um contexto de dispositivo.                                                                            |
| [**SetTextJustification**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Especifica a quantidade de espaço que o sistema deve adicionar aos caracteres de quebra em uma cadeia de caracteres.                             |
| [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Grava uma cadeia de caracteres em um local, expandindo guias para valores especificados.                                         |
| [**Texto**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Grava uma cadeia de caracteres em um local.                                                                             |



 

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows.

-   [**CreateScalableFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**EnumFontFamProc**](/previous-versions//dd162621(v=vs.85))
-   [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**EnumFontsProc**](/previous-versions//dd162623(v=vs.85))
-   [**GetCharWidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
