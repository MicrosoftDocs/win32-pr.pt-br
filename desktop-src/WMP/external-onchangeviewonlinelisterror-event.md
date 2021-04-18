---
title: Evento external. OnChangeViewOnlineListError
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Evento external. OnChangeViewOnlineListError do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789542"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Evento external. OnChangeViewOnlineListError

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnChangeViewOnlineListError** ocorre quando uma chamada para o método [external. changeViewOnlineList](external-changeviewonlinelist.md) resulta em um erro.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse erro tem os parâmetros a seguir.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Human*
</dt> <dd>

Um código de falha **HRESULT** que indica o motivo da falha.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationType** de **changeViewOnlineList**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationID** de **changeViewOnlineList**.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **params** de **changeViewOnlineList**.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **FriendlyName** de **changeViewOnlineList**.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **ListType** de **changeViewOnlineList**.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **ViewMode** de **changeViewOnlineList**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





