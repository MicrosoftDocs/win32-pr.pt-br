---
title: Elemento DropDownButton
description: Representa um controle Drop-Down Button padrão.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Elemento DropDownButton Windows Ribbon
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3275e6de398c42d29424b2a1f9b0c750989357ef21c10d5db1e1680e7adb0836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707264"
---
# <a name="dropdownbutton-element"></a>Elemento DropDownButton

Representa um controle [de botão de lista](windowsribbon-controls-dropdownbutton.md) listada padrão.

## <a name="usage"></a>Uso

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
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
<td>Válido somente se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> for o elemento pai.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                             | Descrição                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| **DropDownButton**<br/>                                                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                     | Deve ocorrer pelo menos uma vez<br/> <br/>    |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| **DropDownButton**<br/>                                                     |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Grupo**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional ou obrigatório, dependendo do elemento pai.

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

**DropDownButton dá** suporte [a modos de](ribbon-applicationmodes.md) aplicativo quando ele é hospedado na coluna esquerda do Menu do Aplicativo.

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) e [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) não são elementos filho válidos de **DropDownButton** quando **DropDownButton** é um descendente de [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para **o DropDownButton.**

Esta seção de código mostra as declarações de Comando [](windowsribbon-element-group.md) **DropDownButton,** com um Grupo associado que funciona como o contêiner pai para o **elemento DropDownButton.**


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



Esta seção de código mostra as **declarações de controle DropDownButton.**


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de botão de lista baixa](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

