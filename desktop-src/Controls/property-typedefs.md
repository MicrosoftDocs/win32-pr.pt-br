---
title: Identificadores de propriedade (Windows controles)
description: Este tópico contém informações sobre valores definidos que são usados para recuperar propriedades de estilos visuais. As definições são encontradas em Vssym32.h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf20429d5eb5bd45ea850e3b77c5734ab6b8e0fa0e63fe4c1d2b1c918f837f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078860"
---
# <a name="property-identifiers-windows-controls"></a>Identificadores de propriedade (Windows controles)

Este tópico contém informações sobre valores definidos que são usados para recuperar propriedades de estilos visuais. As definições são encontradas em Vssym32.h.

## <a name="property-types"></a>Tipos de propriedade

A tabela a seguir lista os tipos de propriedade primitivos. Os valores na primeira coluna normalmente não são usados por aplicativos, mas fornecem um meio de classificar identificadores de propriedade.



| Tipo de Dados       | Descrição                              | Tipo retornado                          | Função de recuperação                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ BOOL       | **TRUE** ou **FALSE**                    | Boolean                                | [**GetThemeBool,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool) [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| COR da \_ TMT      | Valor de cor RGB                          | [**Estrutura COLORREF**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Fluxo de disco                              | **Hinstance**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| TMT \_ ENUM       | Valor enumerado                         | Enumeração                            | [**GetThemeEnumValue.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue)                                                                        |
| TMT \_ FILENAME   | Nome do arquivo em relação ao diretório de tema | **Matriz WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| FONTE \_ TMT       | Descrição da fonte                         | [**Estrutura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)   | [**GetThemeFont,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont) [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | Bitmap                                   | **Alça HBITMAP**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ INT        | Número assinado                            | Integer                                | [**GetThemeInt,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint) [**GetThemeSysInt,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint) [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ INTLIST    | Lista de inteiros                         | [**Estrutura INTLIST**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| MARGENS DO TMT \_    | Margens: esquerda, superior, direita e inferior    | [**Estrutura MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| POSIÇÃO DO \_ TMT   | Local de um item                      | [**Estrutura POINT**](/previous-versions//dd162805(v=vs.85))       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ RECT       | Tamanho e localização de um retângulo         | [**Estrutura RECT**](/previous-versions//dd162897(v=vs.85))         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| TAMANHO DA \_ TMT       | Tamanho de um item                          | [**Estrutura SIZE**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| CADEIA DE CARACTERES TMT \_     | Cadeia de caracteres Unicode                           | **Matriz WCHAR**                        | [**GetThemeString,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring) [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>IDs de propriedade

A seguir estão os valores definidos para propriedades de tema, agrupadas por tipo de dados.

**TMT \_ BOOL**



| ID                        | Observações                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **TRUE** se a barra deizing associada à parte e ao estado sempre deve ser mostrada.                                                                                                                           |
| TMT \_ AUTOSIZE             | **TRUE** se a área de legenda não dependente associada à parte e ao estado variar com a largura do texto.                                                                                                                 |
| TMT \_ BGFILL               | **TRUE** se as imagens de tamanho verdadeiro associadas à parte e ao estado devem ser desenhadas no preenchimento da plano de fundo.                                                                                                        |
| TMT \_ BORDERONLY           | **TRUE** se a imagem associada à parte e ao estado deve ter apenas sua borda desenhada.                                                                                                                     |
| TMT \_ COMPOSITED           | **TRUE** se o controle associado à parte e ao estado tratará sua própria composição de imagens.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| TMT \_ DRAWBORDERS          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | Consulte [**GetThemeSysBool.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                                                                                                                                                 |
| \_GLIFOL TMT            | **TRUE** se o glifo associado à parte e ao estado deve ser desenhado sem uma segundo plano.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **TRUE** se o glifo associado à parte e ao estado tiver áreas transparentes. Consulte [**GetThemeColor para**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) obter a definição do valor de TMT \_ GLYPHCOLOR que define a cor transparente. |
| INTEGRALIZAÇÃO DE TMT \_       | **TRUE** se a imagem truesize ou a borda associada à parte e ao estado devem ser dimensionados para um fator de 2.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **TRUE** se a imagem associada à parte e ao estado deve ser invertida se a janela estiver sendo exibida no modo de leitura da direita para a esquerda.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **True** se a imagem associada à parte e ao estado for dimensionada em tamanho maior se necessário.                                                                                                                |
| TMT \_ SOURCESHRINK         | **True** se a imagem associada à parte e ao estado for menor do que o tamanho, se necessário.                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| textbrilhantes TMT \_             |                                                                                                                                                                                                                 |
| TMT \_ TEXTitalic           |                                                                                                                                                                                                                 |
| TMT \_ transparente          |                                                                                                                                                                                                                 |
| TMT \_ UNIFORMSIZING        | **True** se a imagem associada à parte e ao estado precisar ter altura e largura iguais.                                                                                                                      |
| TMT \_ USERpicture          | **True** se a imagem associada à parte e ao estado for baseada no usuário atual.                                                                                                                          |



 

**\_cor TMT**



| ID                           | Observações                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | A cor usada como uma dica de cor de destaque para controles personalizados.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| TMT \_ plano de fundo              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | A cor usada como uma cor de mesclagem.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| \_BORDERCOLOR TMT             | A cor da borda associada à parte e ao estado.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | A cor usada como uma dica de cor de borda para controles personalizados.                                                                                                                                     |
| TMT \_ btnface                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BtnText                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | A cor da sombra escura da borda associada a esta parte e o estado.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | A cor de preenchimento da borda associada a esta parte e estado.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | A cor de realce da borda associada a esta parte e o estado.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | A cor clara da borda associada a esta parte e estado.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | A cor da sombra da borda associada a esta parte e estado.                                                                                                                              |
| TMT \_ FILLCOLOR               | A cor do preenchimento do plano de fundo associado à parte e ao estado.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | A cor usada como uma dica de cor de preenchimento para controles personalizados.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | A cor do brilho produzida chamando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) usando esta parte e estado.                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | A cor em que o glifo baseado em fonte associado a esta parte e o estado será usado.                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | A cor de glifo transparente associada a esta parte e estado. Se o \_ valor de GLYPHTRANSPARENT TMT para essa parte e o estado for **true**, partes do glifo que usam essa cor não serão desenhadas. |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | A primeira cor do gradiente associado a esta parte e estado.                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | A segunda cor do gradiente.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | A terceira cor do gradiente.                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | A quarta cor do gradiente.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | A quinta cor do gradiente.                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ realce               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| \_menu TMT                    |                                                                                                                                                                                                |
| TMT \_ MenuBar                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| TMT \_ ScrollBar               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | A cor da sombra desenhada sob o texto associado a esta parte e estado.                                                                                                             |
| textbordercolor TMT \_         | A cor da borda do texto associada a esta parte e estado.                                                                                                                              |
| TMT \_ TEXTCOLOR               | A cor do texto associado a esta parte e estado.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | A cor da sombra de texto associada a esta parte e estado.                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | A cor transparente associada a essa parte e estado. Se o valor TMT TRANSPARENT dessa parte e estado for TRUE, as partes do gráfico que \_ usam essa cor não serão desenhadas.           |
| JANELA \_ TMT                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| ID              | Observações |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**TMT \_ ENUM**



| Enumeração         | Valores da propriedade                                                                                                                                                                                                                                            | Observações                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | O tipo de desenho básico para esta parte.                                                                                                                |
| Bordertype          | BT \_ RECT, BT \_ ROUNDRECT, BT \_ ELLIPSE                                                                                                                                                                                                                       | O tipo de borda desenhada se esta parte for um preenchimento de borda.                                                                                              |
| Contentalignment    | CA \_ LEFT, CA \_ CENTER, CA \_ RIGHT                                                                                                                                                                                                                            | O alinhamento do texto na legenda associada a esta parte.                                                                                      |
| Filltype            | FT \_ SOLID, FT \_ VERTGRADIENT, FT \_ HORZGRADIENT, FT \_ RADIALGRADIENT, FT \_ TILEIMAGE                                                                                                                                                                           | O tipo de forma de preenchimento desenhada se essa parte for um preenchimento de borda.                                                                                          |
| Glyphtype           | GT \_ NONE, GT \_ IMAGEGLYPH, GT \_ FONTGLYPH                                                                                                                                                                                                                    | O tipo de glifo desenhado nesta parte.                                                                                                                |
| Glyphfontsizingtype | GFST \_ NONE, GFST \_ SIZE, GFST \_ DPI                                                                                                                                                                                                                          | O tipo de método usado para selecionar entre glifos de tamanho diferente.                                                                                    |
| HALIGN              | HA \_ LEFT, HA \_ CENTER, HA \_ RIGHT                                                                                                                                                                                                                            | O alinhamento horizontal se essa parte usar uma imagem de tamanho verdadeiro.                                                                                        |
| Iconeffect          | ICE \_ NONE, \_ ICE BRILHO, ICE \_ SHADOW, ICE \_ PULSE, ICE \_ ALPHA                                                                                                                                                                                                  | O tipo de efeito a ser exibido quando essa parte é desenhada [**usando DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| Imagelayout         | IL \_ VERTICAL, IL \_ HORIZONTAL                                                                                                                                                                                                                               | O tipo de alinhamento usado quando várias imagens são desenhadas.                                                                                           |
| Imageselecttype     | IST \_ NONE, IST \_ SIZE, IST \_ DPI                                                                                                                                                                                                                             | O tipo de método usado para selecionar entre imagens dimensionada para esta parte. Consulte o valor imageFILE1 do TMT \_ [**de GetThemeFilename.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename) |
| OFFSETTYPE          | OT \_ TOPLEFT, OT \_ TOPRIGHT, OT \_ TOPMIDDLE, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT \_ MIDDLERIGHT, OT \_ LEFTOFCAPTION, OT \_ RIGHTOFCAPTION, OT \_ LEFTOFLASTBUTTON, OT \_ RIGHTOFLASTBUTTON, OT \_ ABOVELASTBUTTON, OT \_ BELOWLASTBUTTON | O alinhamento dessa parte na janela.                                                                                                            |
| Sizingtype          | ST \_ TRUESIZE, ST \_ STRETCH, ST \_ TILE, ST \_ TILEHORZ, ST \_ TILEVERT, ST \_ TILECENTER                                                                                                                                                                            | O método usado para tamanho de uma imagem se essa parte usar um arquivo de imagem.                                                                                    |
| Textshadowtype      | TST \_ NONE, TST \_ SINGLE, TST \_ CONTINUOUS                                                                                                                                                                                                                    | O tipo de efeito de sombra para desenhar atrás do texto associado a esta parte.                                                                             |
| Truesizescalingtype | TSST \_ NONE, TSST \_ SIZE, TSST \_ DPI                                                                                                                                                                                                                          | O tipo de dimensionamento usado se essa parte usar uma imagem de tamanho verdadeiro.                                                                                       |
| Valign              | VA \_ TOP, VA \_ CENTER, VA \_ BOTTOM                                                                                                                                                                                                                            | O alinhamento vertical se essa parte usar uma imagem de tamanho verdadeiro.                                                                                          |



 

**TMT \_ FILENAME**



| ID                  | Observações                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYFILE | O nome do arquivo para a imagem de glifo associada a essa parte e estado.                                                                        |
| TMT \_ IMAGEFILE      | O nome do arquivo da imagem associada a essa parte e estado ou o nome de arquivo base para várias imagens associadas a essa parte e estado. |
| TMT \_ IMAGEFILE1     | O nome do arquivo da primeira imagem dimensionada associada a essa parte e estado, para dar suporte a resoluções diferentes.                            |
| TMT \_ IMAGEFILE2     | O nome do arquivo da segunda imagem dimensionada.                                                                                                     |
| TMT \_ IMAGEFILE3     | O nome do arquivo da terceira imagem dimensionada.                                                                                                      |
| TMT \_ IMAGEFILE4     | O nome do arquivo da quarta imagem dimensionada.                                                                                                     |
| TMT \_ IMAGEFILE5     | O nome do arquivo da quinta imagem dimensionada.                                                                                                      |



 

**FONTE \_ TMT**



| ID                    | Observações                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| GLIFONT \_ TMT        | A fonte com a que o glifo associado a essa parte será desenhada, se glifos baseados em fonte são usados. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| ÍCONE DE \_ TMTTITLEFONT    |                                                                                                      |
| \_MENU TMTFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| STATUS DO \_ TMTFONT       |                                                                                                      |



 

**TMT \_ INT**



| ID                       | Observações                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | O valor alfa (0-255) usado [**para DrawThemeIcon.**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon)                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | O valor alfa mínimo (0-255) que um pixel deve ter para ser considerado opaco.                                                                                                                                  |
| ANIMAÇÃO \_ TMTDELAY      |                                                                                                                                                                                                                  |
| ANIMAÇÃO \_ TMTDURATION   |                                                                                                                                                                                                                  |
| TMT \_ BORDERSIZE          | A espessura da borda desenhada se essa parte usa um preenchimento de borda.                                                                                                                                               |
| conjunto de \_ caracteres TMT             |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| TMT \_ FRAMESPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | O índice de caracteres na fonte selecionada que será usada para o glifo, se a parte usar um glifo baseado em fonte.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | A quantidade da primeira cor de gradiente (TMT \_ GRADIENTCOLOR1) a ser usada no desenho da parte. Esse valor pode ser de 0 a 255, mas esse valor mais os valores de cada um dos valores de GRADIENTRATIO devem ser somados a 255. |
| TMT \_ GRADIENTRATIO2      | A quantidade da segunda cor de gradiente (TMT \_ GRADIENTCOLOR2) a ser usada no desenho da parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | A quantidade da terceira cor de gradiente (TMT \_ GRADIENTCOLOR3) a ser usada no desenho da parte.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | A quantidade da quarta cor de gradiente (TMT \_ GRADIENTCOLOR4) a ser usada no desenho da parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | A quantidade da quinta cor de gradiente (TMT \_ GRADIENTCOLOR5) a ser usada no desenho da parte.                                                                                                                         |
| altura de TMT \_              | A altura da parte.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | O número de imagens de estado presentes em um arquivo de imagem.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | O mínimo de pontos por polegada (DPI) para o qual o primeiro arquivo de imagem foi projetado.                                                                                                                                      |
| TMT \_ MINDPI2             | O DPI mínimo para o qual o segundo arquivo de imagem foi projetado.                                                                                                                                                     |
| TMT \_ MINDPI3             | O mínimo de dpi para o qual o terceiro arquivo de imagem foi projetado.                                                                                                                                                      |
| TMT \_ MINDPI4             | O DPI mínimo para o qual o quarto arquivo de imagem foi projetado.                                                                                                                                                     |
| TMT \_ MINDPI5             | O mínimo de dpi para o qual o quinto arquivo de imagem foi projetado.                                                                                                                                                      |
| opacidade de TMT \_             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | O tamanho das formas "partes" do controle de progresso que definem a distância em que uma operação foi progredida.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | O tamanho total de todas as "partes" do controle de progresso.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | O arredondamento (de 0 a 100 por cento) dos cantos da parte.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | O arredondamento (de 0 a 100 por cento) dos cantos da parte.                                                                                                                                                          |
| saturação de TMT \_          | A quantidade de saturação (0-255) a ser aplicada a um ícone desenhado usando [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
| \_TEXTborderize TMT      | A espessura da borda desenhada em torno de caracteres de texto.                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ TRUESIZESTRETCHMARK | A porcentagem de tamanho original de uma imagem de tamanho real na qual a imagem será ampliada.                                                                                                                        |
| largura de TMT \_               | A largura da parte.                                                                                                                                                                                           |



 

**TMT \_ intl**



| ID                       | Observações |
|--------------------------|-------|
| TMT \_ TRANSITIONDURATIONS |       |



 

**\_margens TMT**



| ID                  | Observações                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | As margens que definem onde o texto da legenda pode ser colocado dentro de uma parte. |
| TMT \_ CONTENTMARGINS | As margens que definem onde o conteúdo pode ser colocado dentro de uma parte.      |
| TMT \_ SIZINGMARGINS  | As margens usadas para dimensionar uma imagem de tamanho não real.                      |



 

**\_posição TMT**



| ID                    | Observações                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MINSIZE          | O tamanho mínimo que o arquivo de imagem normal pode ser usado antes de passar para o próximo arquivo de imagem menor.   |
| TMT \_ MINSIZE1         | O tamanho mínimo para o qual o primeiro arquivo de imagem pequena pode ser usado.                                            |
| TMT \_ MINSIZE2         | O tamanho mínimo para o qual o segundo arquivo de imagem pequena pode ser usado.                                           |
| TMT \_ MINSIZE3         | O tamanho mínimo para o qual o terceiro arquivo de imagem pequena pode ser usado.                                            |
| TMT \_ MINSIZE4         | O tamanho mínimo para o qual o quarto arquivo de imagem pequena pode ser usado.                                           |
| TMT \_ MINSIZE5         | O tamanho mínimo para o qual o quinto arquivo de imagem pequena pode ser usado.                                            |
| TMT \_ NORMALSIZE       | O tamanho da imagem normal associada a esta parte.                                                      |
| deslocamento de TMT \_           | O deslocamento de posição do alinhamento desta parte. O alinhamento é definido pelo valor de \_ deslocamento TMT. |
| TMT \_ TEXTSHADOWOFFSET | O deslocamento do texto no qual as sombras de texto são desenhadas.                                                    |



 

**TMT \_ Rect**



| ID                       | Observações                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ CUSTOMSPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | O tamanho padrão da parte. |



 

**tamanho do TMT \_**



| ID                      | Observações                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Altura da barra de legenda.       |
| TMT \_ CAPTIONBARWIDTH    | Largura da barra de legenda.        |
| TMT \_ MENUBARHEIGHT      | Altura da barra de menus.          |
| TMT \_ MENUBARWIDTH       | Largura da barra de menus.           |
| TMT \_ PADDEDBORDERWIDTH  | Largura da borda preenchida.      |
| TMT \_ SCROLLBARHEIGHT    | Altura da barra de rolagem.        |
| TMT \_ SCROLLBARWIDTH     | Largura da barra de rolagem.         |
| TMT \_ SIZINGBORDERWIDTH  | Largura de uma borda de dimensionamento. |
| TMT \_ SMCAPTIONBARHEIGHT | Altura da barra de legenda.       |
| TMT \_ SMCAPTIONBARWIDTH  | Largura da barra de legenda.        |



 

**\_cadeia de caracteres TMT**



| ID                   | Observações                                               |
|----------------------|-----------------------------------------------------|
| \_alias TMT           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| autor do TMT \_          |                                                     |
| TMT \_ clássicovalue    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| \_empresa TMT         |                                                     |
| \_direitos autorais do TMT       |                                                     |
| TMT \_ CSSNAME         | Consulte [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| Descrição de TMT \_     |                                                     |
| \_DISPLAYNAME TMT     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| tamanhos de TMT \_           |                                                     |
| \_texto TMT            | O texto exibido pela parte.                     |
| \_dica de ferramenta TMT         |                                                     |
| URL do TMT \_             |                                                     |
| versão do TMT \_         |                                                     |
| XmlName do TMT \_         | Consulte [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| nome do TMT \_            |                                                     |



 

 

 
