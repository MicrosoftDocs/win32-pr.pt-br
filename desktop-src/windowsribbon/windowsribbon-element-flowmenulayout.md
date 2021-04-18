---
title: Elemento FlowMenuLayout
description: Representa um layout horizontal com quebras de linha para itens em uma galeria.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Faixa de FlowMenuLayout do elemento do Windows
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105793205"
---
# <a name="flowmenulayout-element"></a>Elemento FlowMenuLayout

Representa um layout horizontal com quebras de linha para itens em uma galeria.

## <a name="usage"></a>Uso

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
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
<td><strong>Colunas</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número de itens a serem exibidos em uma única linha.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> Qualquer inteiro positivo ou negativo. <br/> O padrão é <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Garra</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Um identificador de redimensionamento anexado ao menu suspenso da galeria. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Vertical<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Canto<br/> </dt> <dd> Padrão. <br/> </dd> </dl></td>
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

O elemento [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou **FlowMenuLayout** deve ocorrer uma vez para cada elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)ou [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

Os elementos são organizados de acordo com as propriedades de quebra de linha inerentes aos atributos de *linha* e *coluna* . Quando o conteúdo excede o comprimento de uma única linha, o menu quebra linhas, delimita linhas e alinha o conteúdo adequadamente.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).

Esta seção de código mostra a declaração de controle [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) com uma especificação **FlowMenuLayout** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Sim       |



 

 





