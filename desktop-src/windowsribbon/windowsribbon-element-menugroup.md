---
title: Elemento MenuGroup
description: Representa um contêiner de controles a ser exibido em uma galeria, menu ou barra de ferramentas.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- Elemento MenuGroup Windows Faixa de Opções
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 854b33d1e11df15b5b383bf004986edc18418f6204ae1298c3171a6653cf5301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707080"
---
# <a name="menugroup-element"></a>Elemento MenuGroup

Representa um contêiner de controles a ser exibido em uma galeria, menu ou barra de ferramentas.

## <a name="usage"></a>Uso

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>Classe</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Especifica o tamanho e o estilo de layout para elementos na interface do usuário do menu.<br/> Um recurso de imagem pode ser fornecido em dois tamanhos (grande e pequeno) e associado ao elemento na marcação usando os elementos de propriedade <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> e <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages.</strong></a> Se apenas uma imagem for fornecida, a estrutura a reorganizará conforme necessário.<br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems)<br/> </dt> <dd> Padrão. <br/> Estilo: imagem pequena e texto desalinhado.<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems)<br/> </dt> <dd> Estilo: imagem grande e texto em negrito.<br/>
<blockquote>
[!Note]<br />
Se <strong>MenuGroup</strong> for um filho de <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu,</strong></a>o atributo <em>Class</em> será ignorado e um estilo de será imposto pela <code>MajorItems</code> estrutura .
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
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
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer pelo menos uma vez para cada [**elemento ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups,**](windowsribbon-element-splitbutton-menugroups.md) [**MiniToolbar**](windowsribbon-element-minitoolbar.md)ou [**SplitButtonGallery.MenuGroups.**](windowsribbon-element-splitbuttongallery-menugroups.md)

Se [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) for o elemento pai, **MenuGroup** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).

Se [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)ou [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) for o elemento pai, **MenuGroup** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).

Se [**MiniToolbar**](windowsribbon-element-minitoolbar.md) for o elemento pai, **MenuGroup** será restrito aos seguintes elementos filho: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)ou [**ToggleButton**](windowsribbon-element-togglebutton.md).

O atributo Class não é necessário quando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) é o elemento pai. A estrutura impõe um valor de MajorItems para o atributo Class.

Quando [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) é o elemento pai, o atributo Class não é necessário.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para [**o SplitButton**](windowsribbon-element-splitbutton.md) com um **elemento MenuGroup.**

Esta seção de código mostra as declarações [**De comando SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** com um recurso de imagem grande e pequeno. Um Grupo associado [**que**](windowsribbon-element-group.md) atua como o contêiner pai para o **elemento SplitButton** também é declarado.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



Esta seção de código mostra as declarações [**de controle SplitButton**](windowsribbon-element-splitbutton.md) e **MenuGroup** com `StandardItems` e `MajorItems` .


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificando recursos de imagem da faixa de opções](windowsribbon-imageformats.md)
</dt> <dt>

[Grupo de Menus](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





