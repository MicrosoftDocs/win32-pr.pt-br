---
description: O método Remove remove o objeto CDeferredCommand da fila.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue.Remove (Winutil.h)
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
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954575"
---
# <a name="ccmdqueueremove-method"></a>Método CCmdQueue.Remove

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

Ponteiro para o **objeto CDeferredCommand** a ser removido da fila.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará VFW \_ E NOT FOUND se o objeto não for encontrado na \_ \_ fila. Caso contrário, retornará S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




