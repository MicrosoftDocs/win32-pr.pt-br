---
description: O método Insert adiciona um objeto CDeferredCommand à fila.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Método CCmdQueue. Insert (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757316"
---
# <a name="ccmdqueueinsert-method"></a>Método CCmdQueue. Insert

O `Insert` método adiciona um objeto [**CDeferredCommand**](cdeferredcommand.md) à fila.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCmd* 
</dt> <dd>

Ponteiro para o objeto **CDeferredCommand** a ser adicionado à fila.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK na implementação padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




