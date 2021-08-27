---
title: Propriedade ApplicationMenu. RecentItems
description: Representa um contêiner para o controle itens recentes no menu do aplicativo.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- propriedade ApplicationMenu. RecentItems Windows Ribbon
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630371"
---
# <a name="applicationmenurecentitems-property"></a>Propriedade ApplicationMenu. RecentItems

Representa um contêiner para o controle [itens recentes](windowsribbon-controls-recentitems.md) no [menu do aplicativo](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
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
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Descrição                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**RecentItems**](windowsribbon-element-recentitems.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .

O controle [itens recentes](windowsribbon-controls-recentitems.md) exibe a lista de itens usados mais recentemente (MRU) do aplicativo da faixa de faixas.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o controle [itens recentes](windowsribbon-controls-recentitems.md) .

O exemplo a seguir mostra uma declaração de comando [**RecentItems**](windowsribbon-element-recentitems.md) .


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



O exemplo a seguir mostra a declaração de controles **ApplicationMenu. RecentItems** e [**RecentItems**](windowsribbon-element-recentitems.md) associados.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de menu do aplicativo](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Controle de itens recentes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





