---
title: Elemento ComboBox
description: Representa um controle Caixa de Combinação.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Elemento ComboBox Windows Ribbon
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ee7a03d25508df45469577f4d4159b5db5f5190f188ca594b71f176d037526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851181"
---
# <a name="combobox-element"></a>Elemento ComboBox

Representa um [controle Caixa de Combinação.](windowsribbon-controls-combobox.md)

## <a name="usage"></a>Uso

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsAutoCompleteEnabled</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Iseditable</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ResizeType</strong><br/></td>
<td>ComboBoxResizeType<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (NoResize)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (VerticalResize)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e mais novos.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

Como o **ComboBox** é exclusivamente uma galeria de itens, ele não dá suporte a itens command. Ele também é o único controle de galeria que não dá suporte a um Espaço de Comando (uma coleção de Comandos que são declarados na marcação e listados na parte inferior de uma galeria de itens ou galeria de comandos). Para obter mais informações, consulte [Trabalhando com galerias.](ribbon-controls-galleries.md)

A captura de tela a seguir ilustra um controle [Caixa de Combinação](windowsribbon-controls-combobox.md) da Faixa de Opções Windows Live Movie Maker.

![captura de tela de um controle de caixa de combinação na faixa de opções de pintura da Microsoft.](images/controls/combobox.png)

## <a name="examples"></a>Exemplos

Os exemplos a seguir demonstram a marcação básica para **o ComboBox.**

Esta seção de código mostra as declarações do Comando [](windowsribbon-element-group.md) **ComboBox,** com um Grupo associado que atua como o contêiner pai para o **elemento ComboBox.**


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



Esta seção de código mostra as **declarações de controle ComboBox.**


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle Caixa de Combinação](windowsribbon-controls-combobox.md)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





