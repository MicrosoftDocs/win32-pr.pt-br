---
description: O método Wait bloqueia até que o evento seja sinalizado ou até que ocorra um tempo-out.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Método CAMEvent.Wait (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3875647cb93619e8326066bc9af7a6f99f79a0b0a2df58f668b1e365fd39102b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662507"
---
# <a name="cameventwait-method"></a>Método CAMEvent.Wait

O `Wait` método bloqueia até que o evento seja sinalizado ou até que ocorra um tempo-out.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dwtimeout* 
</dt> <dd>

Valor de tempo-out opcional, representado em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o evento for sinalizado. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Para eventos de redefinição automática, o evento é redefinido para um estado não sinal quando este método retorna.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




