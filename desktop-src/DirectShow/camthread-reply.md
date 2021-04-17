---
description: O método Reply responde a uma solicitação.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread. Reply (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812996"
---
# <a name="camthreadreply-method"></a>Método CAMThread. Reply

O `Reply` método responde a uma solicitação.

## <a name="syntax"></a>Sintaxe


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dw* 
</dt> <dd>

Valor a ser retornado no método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método CallWorker é bloqueado até que esse método seja chamado. O parâmetro *DW* fornece o valor de retorno para CallWorker. Chame esse método em seu procedimento de thread depois de recuperar uma solicitação, para liberar o thread solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




