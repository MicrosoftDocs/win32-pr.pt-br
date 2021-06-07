---
title: Elemento DropDownColorPicker
description: Representa um Pickercontrol de cor de Drop-Down que, quando clicado, exibe uma paleta de amostras de cor.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Faixa de DropDownColorPicker do elemento do Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442897"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Representa um controle [seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md)que, quando clicado, exibe uma paleta de amostras de cor.

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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><strong>Chips</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>O tamanho de cada amostra ou chip de cor. <br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Menores<br/> </dt> <dd> Cada chip de cor é um quadrado de pixel 11x11. <br/> </dd> <dt><span></span><span></span><strong></strong> Médio<br/> </dt> <dd> Cada chip de cor é um quadrado de 16x16 pixels. <br/> </dd> <dt><span></span><span></span><strong></strong> Vários<br/> </dt> <dd> Cada chip de cor é um quadrado de pixel 24x24. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Cortemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Modelos de layout que especificam o tipo de <a href="windowsribbon-controls-dropdowncolorpicker.md">seletor de cores suspenso</a>. <br/> Restrito a um dos valores a seguir (se nenhum atributo opcional relacionado a um <em>colortemplate</em> for declarado, a exibição padrão será mostrada):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Padrão. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Definir o atributo <em>colortemplate</em> para <code>ThemeColors</code> habilitar a seguinte funcionalidade:<br/>
<ul>
<li>Âncora de SplitButton.</li>
<li>O botão de cor <strong>automático</strong> é exibido por padrão.</li>
<li>Grade de amostras de <strong>cores de tema</strong> do Windows.</li>
<li>Grade de amostra de <strong>cores padrão</strong> .</li>
<li>A grade de amostras de <strong>cores recentes</strong> é opcional.</li>
<li>Iniciador da caixa de diálogo <strong>mais cores</strong> .</li>
<li><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Definir o atributo <em>colortemplate</em> para <code>StandardColors</code> habilitar a seguinte funcionalidade:<br/>
<ul>
<li>Âncora de SplitButton.</li>
<li>O botão de cor <strong>automático</strong> é exibido por padrão.</li>
<li>Grade de amostra de <strong>cores padrão</strong> .</li>
<li>Iniciador da caixa de diálogo <strong>mais cores</strong> .</li>
<li><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Definir o atributo <em>colortemplate</em> para <code>HighlightColors</code> habilitar a seguinte funcionalidade:<br/>
<ul>
<li>Âncora de SplitButton.</li>
<li>Grade de amostra de <strong>cores padrão</strong> sem cabeçalho.</li>
<li><strong>Nenhum</strong> botão de cor de cor é exibido por padrão.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Colunas</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de colunas de chip de cor (ou amostra).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Exibe (ou oculta) o botão de cor <strong>automática</strong> . <br/> Válido somente quando <code>StandardColors</code> ou <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> . <br/> Restrito a um dos valores a seguir (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Exibe (ou oculta) o botão <strong>sem cor</strong> . <br/> Válido para todos os valores de <em>colortemplate</em> .<br/> Restrito a um dos valores a seguir (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cor (ou amostra) na área <strong>cores recentes</strong> . <br/> Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cor (ou amostra) na área <strong>cores padrão</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O número de linhas de chip de cor (ou amostra) na área <strong>cores do tema</strong> .<br/> Válido somente quando <code>ThemeColors</code> é especificado para o atributo <em>colortemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer valor inteiro positivo entre 1 e 256, inclusive.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**Controlador de controle**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Grupo**](windowsribbon-element-group.md)<br/>                           |
| [**Grupo Backstage**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md)Group [**, DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para todos os três tipos de [seletor de cor suspenso](windowsribbon-controls-dropdowncolorpicker.md).

Esta seção de código mostra as declarações de comando para três elementos **DropDownColorPicker** .


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



Esta seção de código mostra os três tipos de declarações de controle **DropDownColorPicker** .


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

* **Sistema mínimo com suporte**: Windows 7
* **Pode estar vazio**: Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Exemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





