---
title: Elemento RecentItems
description: Representa o controle Itens Recentes no Menu do Aplicativo.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Elemento RecentItems Windows Faixa de Opções
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae49864fea057aa942b121f21813acfd0f26c6cc4411d4f1b3c59cda12014c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881556"
---
# <a name="recentitems-element"></a>Elemento RecentItems

Representa o [controle Itens Recentes](windowsribbon-controls-recentitems.md) no Menu do [Aplicativo](windowsribbon-controls-applicationmenu.md).

## <a name="usage"></a>Uso

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
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
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>Não<br/></td>
<td>O número de itens recentes a exibir.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)<br/> </dt> <dd> Um valor inteiro de 0 ou maior.<br/> O padrão é <strong>10</strong>.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para [**cada elemento ApplicationMenu.RecentItems.**](windowsribbon-element-applicationmenu-recentitems.md)

O [controle Itens Recentes](windowsribbon-controls-recentitems.md) exibe a lista de itens de MRU (itens usados mais recentemente) do aplicativo Ribbon.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [controle Itens](windowsribbon-controls-recentitems.md) Recentes.

O exemplo a seguir mostra uma **declaração de Comando RecentItems.**


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



O exemplo a seguir mostra a declaração **de controles RecentItems** associada.


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Sim


## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de Menu do Aplicativo](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[Controle itens recentes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





