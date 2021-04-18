---
title: Evento external. OnChangeViewError
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Evento external. OnChangeViewError do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789543"
---
# <a name="externalonchangeviewerror-event"></a>Evento external. OnChangeViewError

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnChangeViewError** ocorre quando uma chamada para o método [external. changeView](external-changeview.md) resulta em um erro.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento tem os parâmetros a seguir.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Human*
</dt> <dd>

Um código de falha **HRESULT** que indica o motivo da falha.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **LibraryLocationType** de **changeView**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

A mesma cadeia de caracteres thatwas passada no parâmetro **LibraryLocationID** de **changeView**.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Sem*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro de **filtro** de **changeView**.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **ViewParams** de **changeView**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Externalobject para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





