---
title: Elemento Group
description: Representa um controle de grupo que funciona como um contêiner para um grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Faixa de das janelas do elemento de grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366339"
---
# <a name="group-element"></a>Elemento Group

Representa um controle de [grupo](windowsribbon-controls-group.md) que funciona como um contêiner para um grupo de elementos.

## <a name="usage"></a>Uso

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Quando especificado, o valor de <em>SizeDefinition</em> é restrito a um dos <a href="windowsribbon-templates.md">modelos de layout</a> definidos pela estrutura da faixa de opção. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Qualquer sequência de zero ou mais caracteres.<br/> O comprimento máximo é não associado.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                             | Descrição                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Controlador de controle**](windowsribbon-element-controlgroup.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**Controle giratório**](windowsribbon-element-spinner.md)<br/>                         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                             |
|-----------------------------------------------------|
| [**Tab**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada elemento de [**guia**](windowsribbon-element-tab.md) .

[**Guia**](windowsribbon-element-tab.md) dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).

A marcação da faixa de faixas é válida somente quando os elementos filho do **grupo** correspondem ao modelo especificado para *SizeDefinition*.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir ilustra o uso de um modelo personalizado em um **grupo**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> <dt>

[Controle de grupo](windowsribbon-controls-group.md)
</dt> <dt>

[**Setmodos**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

