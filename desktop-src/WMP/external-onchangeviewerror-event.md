---
title: Evento External.OnChangeViewError
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento External.OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Evento External.OnChangeViewError Windows Media Player
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
ms.openlocfilehash: aaa1152c753501b2e2385de8c56af614d62cfb367fcca8468aaa032e9536e8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648826"
---
# <a name="externalonchangeviewerror-event"></a>Evento External.OnChangeViewError

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **evento OnChangeViewError** ocorre quando uma chamada para o [método External.changeView](external-changeview.md) resulta em um erro.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que Windows Media Player chamadas quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que trata esse evento tem os seguintes parâmetros.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Um **código de falha HRESULT** que indica o motivo da falha.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no **parâmetro LibraryLocationType** de **changeView.**

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

A mesma cadeia de caracteres passada no **parâmetro LibraryLocationID** de **changeView.**

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtro*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no **parâmetro Filter** de **changeView.**

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **ViewParams** de **changeView.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExternalObject para Lojas Online do Tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





