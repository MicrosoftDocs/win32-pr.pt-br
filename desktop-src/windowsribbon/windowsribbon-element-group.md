---
title: Elemento Group
description: Representa um controle Group que funciona como um contêiner para um grupo de elementos.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Faixa de opções do Windows grupo
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ca9d138e18296bc801fd37931a3b8066761abd3dd697d360513983ad5288dfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810606"
---
# <a name="group-element"></a>Elemento Group

Representa um [controle](windowsribbon-controls-group.md) Group que funciona como um contêiner para um grupo de elementos.

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
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Quando especificado, o valor de <em>SizeDefinition</em> é restrito a um dos <a href="windowsribbon-templates.md">modelos de layout definidos</a> pela estrutura ribbon. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Qualquer sequência de zero ou mais caracteres.<br/> O comprimento máximo não é desaconsudido.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                             | Descrição                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |
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

Pode ocorrer uma ou mais vezes para cada [**elemento Tab.**](windowsribbon-element-tab.md)

[**A guia**](windowsribbon-element-tab.md) dá suporte [aos modos de aplicativo](ribbon-applicationmodes.md).

A marcação Faixa de Opções é válida somente quando os elementos filho de **Group** correspondem ao modelo especificado para *SizeDefinition.*

## <a name="examples"></a>Exemplos

O exemplo de código a seguir ilustra o uso de um modelo personalizado em um **Grupo**.


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md)
</dt> <dt>

[Controle de grupo](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

