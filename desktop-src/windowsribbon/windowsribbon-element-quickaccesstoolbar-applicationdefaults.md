---
title: Propriedade QuickAccessToolbar. ApplicationDefaults
description: Representa um contêiner para comandos padrão na barra de ferramentas de acesso rápido (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Faixa de QuickAccessToolbar de propriedades do Windows. ApplicationDefaults
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764488"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Propriedade QuickAccessToolbar. ApplicationDefaults

Representa um contêiner para comandos padrão na [barra de ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md).

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



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
<td><a href="windowsribbon-element-button.md"><strong>Botão</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 e mais recente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 e mais recente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 e mais recente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 e mais recente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>Deve ocorrer pelo menos uma vez.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Um mínimo de um elemento filho deve ser especificado.

Um máximo de 20 elementos filho pode ser especificado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Esta seção de código mostra a declaração de controle **QuickAccessToolbar. ApplicationDefaults** .


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





