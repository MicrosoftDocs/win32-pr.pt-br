---
description: O método remove remove o objeto CDeferredCommand da fila.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue. Remove (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748207"
---
# <a name="ccmdqueueremove-method"></a>Método CCmdQueue. Remove

O `Remove` método remove o objeto [**CDeferredCommand**](cdeferredcommand.md) da fila.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCmd* 
</dt> <dd>

Ponteiro para o objeto **CDeferredCommand** a ser removido da fila.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna VFW \_ E \_ não \_ encontrado se o objeto não for encontrado na fila. Caso contrário, retornará S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




