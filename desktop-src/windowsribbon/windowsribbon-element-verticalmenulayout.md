---
title: Elemento VerticalMenuLayout
description: Representa um layout vertical de itens em uma galeria.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Faixa de VerticalMenuLayout do elemento do Windows
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2020
ms.locfileid: "103640360"
---
# <a name="verticalmenulayout-element"></a>Elemento VerticalMenuLayout

Representa um layout vertical de itens em uma galeria.

## <a name="usage"></a>Uso

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
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
<td><strong>Garra</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Um identificador de redimensionamento anexado ao menu suspenso da galeria. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Vertical<br/> </dt> <dd> Padrão. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>Não<br/></td>
<td><strong>Windows 8 e mais recente</strong><br/> Realça todos os itens na lista até, e incluindo, o item atual de mouseover (em vez do item de mouseover somente). Normalmente usado para várias funcionalidades de <strong>desfazer</strong> e <strong>refazer</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd> Padrão. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Linhas</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número de linhas de item a serem visíveis sem rolagem. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Qualquer inteiro positivo ou negativo. <br/> O padrão é <strong>-1</strong> , que especifica a exibição de quantas linhas de item possível.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

O elemento **VerticalMenuLayout** ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deve ocorrer uma vez para cada elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para um elemento **VerticalMenuLayout** .

Esta seção de código mostra as declarações de controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Sim       |



 

 





