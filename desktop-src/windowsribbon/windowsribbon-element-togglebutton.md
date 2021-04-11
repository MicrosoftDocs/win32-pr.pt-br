---
title: Elemento ToggleButton
description: Representa um controle de botão de alternância.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Faixa de das janelas do elemento ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104293726"
---
# <a name="togglebutton-element"></a>Elemento ToggleButton

Representa um controle de [botão de alternância](windowsribbon-controls-togglebutton.md) .

## <a name="usage"></a>Uso

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>ApplicationDefaults. IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Esse atributo é válido somente quando o elemento <strong>ToggleButton</strong> é filho de <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. ApplicationDefaults</strong></a>. <br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**Controlador de controle**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Grupo**](windowsribbon-element-group.md)<br/>                                                                   |
| [**Grupo Backstage**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Comentários

Opcional ou obrigatório, dependendo do elemento pai.

Pode ocorrer no máximo uma vez para cada elemento [**SplitButton. ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) .

Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**menu**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)ou [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o elemento **ToggleButton** .

Esta seção de código mostra uma declaração de elemento **ToggleButton** dentro do elemento [**QuickAccessToolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .


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



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Sim       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de botão de alternância](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





