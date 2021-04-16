---
description: O método checktime determina se um tempo especificado é devido.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Método CCmdQueue. checktime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775638"
---
# <a name="ccmdqueuechecktime-method"></a>Método CCmdQueue. checktime

O `CheckTime` método determina se um tempo especificado é devido.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*time* 
</dt> <dd>

Tempo para verificar.

</dd> <dt>

*bStream* 
</dt> <dd>

**True** se o parâmetro *time* for um valor de tempo de fluxo; **False** se o *tempo* for um valor de tempo de apresentação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o tempo especificado ainda não tiver passado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




