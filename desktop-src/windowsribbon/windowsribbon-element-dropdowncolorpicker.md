---
title: Elemento DropDownColorPicker
description: Representa um Drop-Down controle seletor de cores que, quando clicado, exibe uma paleta de travas de cores.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Elemento DropDownColorPicker Windows Faixa de Opções
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31525ee1b7233f0bf49668856d917ef14bc034b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622882"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Representa um [controle de lista Seletor de Cor](windowsribbon-controls-dropdowncolorpicker.md)que, quando clicado, exibe uma paleta de travas de cores.

## <a name="usage"></a>Uso

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ChipSize</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>O tamanho de cada chip de cor ou amostra. <br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Pequeno)<br/> </dt> <dd> Cada chip de cores é um quadrado de 11 x 11 pixels. <br/> </dd> <dt><span></span><span></span><strong></strong> (Médio)<br/> </dt> <dd> Cada chip de cores é um quadrado de 16 x 16 pixels. <br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Cada chip de cores é um quadrado de 24 x 24 pixels. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Modelos de layout que especificam o tipo de <a href="windowsribbon-controls-dropdowncolorpicker.md">lista Seletor de Cor</a>. <br/> Restrito a um dos seguintes valores (se nenhum atributos opcionais relacionados a <em>um ColorTemplate</em> for declarado, a exibição padrão será mostrada):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Padrão. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Definir o <em>atributo ColorTemplate</em> como <code>ThemeColors</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li>Âncora SplitButton.</li>
<li><strong>O botão</strong> Cor automática é exibido por padrão.</li>
<li>Windows Grade de amostra <strong>de</strong> cores do tema.</li>
<li><strong>Grade de amostra</strong> de cores padrão.</li>
<li><strong>A grade de</strong> amostra Cores Recentes é opcional.</li>
<li><strong>Iniciador da caixa</strong> de diálogo Mais cores.</li>
<li><strong>Nenhum botão</strong> de cor é exibido por padrão.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Definir o <em>atributo ColorTemplate</em> como <code>StandardColors</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li>Âncora SplitButton.</li>
<li><strong>O botão</strong> Cor automática é exibido por padrão.</li>
<li><strong>Grade de amostra</strong> de cores padrão.</li>
<li><strong>Iniciador da caixa</strong> de diálogo Mais cores.</li>
<li><strong>Nenhum botão</strong> de cor é exibido por padrão.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Definir o <em>atributo ColorTemplate</em> como <code>HighlightColors</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li>Âncora SplitButton.</li>
<li><strong>Grade de</strong> amostra de cores padrão sem nenhum header.</li>
<li><strong>Nenhum botão</strong> de cor é exibido por padrão.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Colunas</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de colunas de chip de cores (ou swatch).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Exibe (ou oculta) o <strong>botão Cor</strong> automática. <br/> Válido somente quando <code>StandardColors</code> ou é especificado para o atributo <code>ThemeColors</code> <em>ColorTemplate.</em> <br/> Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Exibe (ou oculta) o <strong>botão Sem</strong> cor. <br/> Válido para todos os <em>valores colorTemplate.</em><br/> Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cores (ou amostra) na <strong>área Cores</strong> recentes. <br/> Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cores (ou swatch) na <strong>área Cores</strong> padrão.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cores (ou swatch) na área <strong>Cores do</strong> tema.<br/> Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Grupo**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para todos os três tipos de [lista Seletor de Cor](windowsribbon-controls-dropdowncolorpicker.md).

Esta seção de código mostra as declarações command para três **elementos DropDownColorPicker.**


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



Esta seção de código mostra os três tipos de declarações **de controle DropDownColorPicker.**


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de Seletor de Cor lista listada](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Exemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





