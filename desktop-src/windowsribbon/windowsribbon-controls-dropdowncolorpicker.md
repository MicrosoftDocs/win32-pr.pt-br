---
title: Drop-Down Seletor de Cor
description: A Windows faixa de opções do Drop-Down Seletor de Cor fornece um controle de Drop-Down Seletor de Cor especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e seletor de cores de lista listada personalizável.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8104ba92d0be9d56607083508d7f30728a7f3a141839d74314561d392fb942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707650"
---
# <a name="drop-down-color-picker"></a>Drop-Down Seletor de Cor

A Windows faixa de opções do Drop-Down Seletor de Cor fornece um controle de Drop-Down Seletor de Cor especializado que expõe uma variedade de configurações de cores por meio de um botão de divisão e seletor de cores de lista listada personalizável.

-   [Introdução](#introduction)
-   [Marcação](#markup)
-   [Código](#code)
    -   [Propriedades](#properties)
    -   [Manipuladores de comandos](#command-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Ao emular a aparência e a funcionalidade do selador de cores Microsoft Office, a estrutura da Faixa de Opções pode se beneficiar e contribuir com a consistência e a familiaridade em uma ampla variedade de aplicativos.

## <a name="markup"></a>Marcação

Como todos os controles de Faixa de Opções, Drop-Down Seletor de Cor é facilmente implementado e personalizado por meio da marcação. A estrutura fornece vários atributos de elemento para o Drop-Down Seletor de Cor expor vários níveis de funcionalidade. A tabela a seguir lista os Drop-Down Seletor de Cor atributos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorTemplate</td>
<td>Modelos de layout que especificam o tipo de Drop-Down Seletor de Cor.<br/> Há três modelos, cada um especificando um layout de controle e valores padrão para atributos associados e chaves de propriedade. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>ChipSize</td>
<td>O tamanho de cada chip de cor (ou amostra).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Colunas</td>
<td>O número de colunas de chip de cores (ou swatch).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>O nome da declaração command associada. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Exibe (ou oculta) o <strong>botão</strong> Automático.<br/> Válido somente quando <em>ColorTemplate</em> tem um valor <code>ThemeColors</code> de ou <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Exibe (ou oculta) o <strong>botão Sem</strong> cor.<br/> Válido para todos os <em>valores colorTemplate.</em><br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>O número de linhas de chip de cores (ou amostra) na <strong>área Cores</strong> recentes.<br/> Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>O número de linhas de chip de cores (ou swatch) na <strong>área Cores</strong> padrão.<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>O número de linhas de chip de cores (ou swatch) na área <strong>Cores do</strong> tema.<br/> Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

As capturas de tela a seguir ilustram os layouts Drop-Down Seletor de Cor padrão para os três modelos de cor.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'themecolors'. ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\] | `standardcolors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\] | `highlightcolors`: \[ captura de tela de nova linha do elemento \] ![ dropdowncolorpicker com o atributo colortemplate definido como 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

A marcação básica necessária para cada tipo Drop-Down Seletor de Cor é demonstrada nos exemplos a seguir:

> [!Note]  
> O Drop-Down Seletor de Cor é um controle [Button](windowsribbon-controls-button.md) válido em um [**modelo SizeDefinition.**](windowsribbon-element-sizedefinition.md)

 


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a>Código

Como um controle especializado que dá suporte à personalização, qualquer implementação do Drop-Down Seletor de Cor que aproveita essas funcionalidades requer um código de aplicativo especializado para gerenciar propriedades e manipular todos os Comandos emitidos pelo controle.

### <a name="properties"></a>Propriedades

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o controle Drop-Down Seletor de Cor.

Normalmente, uma propriedade Drop-Down Seletor de Cor é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao controle Drop-Down Seletor de Cor dados.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Chave de propriedade</th>
<th>Descrição</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Define o rótulo para o <strong>botão Cor</strong> automática.<br/> Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> ou <code>StandardColors</code> .<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Define o valor de cor selecionado como <a href="/windows/win32/gdi/colorref">um COLORREF.</a><br/> Válido somente quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tem um valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Define o tipo de cor selecionado.<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Define a capacidade de um controle responder à interação do usuário.<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Define a cadeia de caracteres para um rótulo de controle.<br/></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Define a imagem de alto contraste grande a ser exibida para um controle .<br/></td>
<td>Só pode ser atualizado por meio de invalidação.<br/> Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Define a imagem grande a ser exibida para um controle .<br/></td>
<td>Só pode ser atualizado por meio de invalidação.<br/> Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">Especificando recursos de</a>imagem da faixa de opções .<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Define o rótulo para o <strong>botão Mais cores....</strong><br/> Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> ou <code>StandardColors</code> .<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Define o rótulo para o <strong>botão Sem</strong> cor.<br/> Válido para todos os <em>valores colorTemplate.</em><br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Define o rótulo para a <strong>categoria Cores recentes.</strong><br/> Válido somente quando <em>ColorTemplate</em> tem um valor de <code>ThemeColors</code> . Esse é o único modelo que contém categorias rotuladas.<br/></td>
<td>Dá <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>suporte a IUIFramework::GetUICommandProperty</strong></a> <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>e IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Define a pequena imagem de alto contraste a ser exibida para um controle.<br/></td>
<td>Só pode ser atualizado por meio de invalidação.<br/> Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Define a imagem pequena a ser exibida para um controle.<br/></td>
<td>Só pode ser atualizado por meio de invalidação.<br/> Para obter mais informações sobre formatos de imagem, consulte <a href="windowsribbon-imageformats.md">especificando recursos de imagem da faixa de Ribbon</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Define uma matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para as amostras de um seletor de cor Drop-Down.<br/> Cada seletor de cor Drop-Down <em>colortemplate</em> contém uma <code>StandardColors</code> grade. <br/>
<blockquote>
[!Note]<br />
Os valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> das colunas <em>StandardColorGridRows</em> x <em></em> iniciais da matriz são exibidos. Se a matriz definir menos cores do que o número de <code>StandardColors</code> amostras declaradas na marcação, espaços vazios serão exibidos para os chips ausentes.
</blockquote>
<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Define o rótulo para a categoria <strong>cores padrão</strong> .<br/> Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> . Esse é o único modelo que contém categorias rotuladas.<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Define uma matriz de cadeia de caracteres de dicas de ferramentas de amostra de cor para a <code>StandardColors</code> grade.<br/> Cada seletor de cor Drop-Down <em>colortemplate</em> contém uma <code>StandardColors</code> grade. <br/>
<blockquote>
[!Note]<br />
Somente as dicas de ferramenta necessárias para rotular as amostras de cor exibidas na <code>StandardColors</code> grade são usadas. Se menos rótulos forem fornecidos do que o número de amostras na <code>StandardColors</code> grade, um padrão será fornecido para as amostras de remainining.
</blockquote>
<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Define uma matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para as amostras de um seletor de cor Drop-Down.<br/> Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Os valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> das colunas <em>ThemeColorGridRows</em> x <em></em> iniciais da matriz são exibidos. Se a matriz definir menos cores do que o número de <code>ThemeColors</code> amostras declaradas na marcação, espaços vazios serão exibidos para os chips ausentes.
</blockquote>
<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Define a matriz de cadeia de caracteres das dicas de ferramentas de amostra de cor para a <code>ThemeColors</code> grade.<br/> Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Somente as dicas de ferramenta necessárias para rotular as amostras de cor exibidas na <code>ThemeColors</code> grade são usadas. Se menos rótulos forem fornecidos do que o número de amostras na <code>ThemeColors</code> grade, um padrão será fornecido para as amostras de remainining.
</blockquote>
<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Define o rótulo para a categoria <strong>cores do tema</strong> .<br/> Válido somente quando <em>colortemplate</em> tem um valor de <code>ThemeColors</code> . Esse é o único modelo que contém categorias rotuladas.<br/></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Define a cadeia de caracteres para uma descrição da dica de ferramenta associada a um <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Define a cadeia de caracteres para uma dica de ferramenta de comando.<br/></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Manipuladores de comandos

O método [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) é usado para personalizar um seletor de cores Drop-Down por meio das chaves de propriedade listadas acima. O exemplo a seguir demonstra como definir as amostras de cor de um seletor de cor Drop-Down, com base em uma preferência de estilo personalizado ou em uma grade de amostra personalizada que é declarada na marcação.


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



O exemplo a seguir demonstra uma implementação do método [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expõe as cores de amostra do seletor de cor Drop-Down para o aplicativo da faixa de opções.


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de controle da estrutura de faixa](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Propriedades do seletor de cores](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> <dt>

[Exemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

