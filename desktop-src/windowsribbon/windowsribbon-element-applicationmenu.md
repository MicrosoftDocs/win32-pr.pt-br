---
title: Elemento ApplicationMenu
description: Representa o Menu do Aplicativo. | Elemento ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Elemento ApplicationMenu Windows Faixa de Opções
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fcf64d3fa3b618a4e66777b8fd4c0d831a33126
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626122"
---
# <a name="applicationmenu-element"></a>Elemento ApplicationMenu

Representa o [Menu do Aplicativo](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                             | Descrição                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada [**Ribbon.ApplicationMenu.**](windowsribbon-element-ribbon-applicationmenu.md)

Os elementos filho do **elemento ApplicationMenu** devem ocorrer na ordem especificada:

1.  [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)
2.  [**Menugroup**](windowsribbon-element-menugroup.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [Menu do Aplicativo](windowsribbon-controls-applicationmenu.md).

Esta seção de código mostra as declarações **do Comando ApplicationMenu.**


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



Esta seção de código mostra as declarações **de controle ApplicationMenu.**


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de Menu do Aplicativo](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





