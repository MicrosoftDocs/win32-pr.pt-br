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
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749023"
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

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK na implementação padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




