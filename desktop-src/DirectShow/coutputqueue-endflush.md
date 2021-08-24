---
description: Método COutputQueue. EndFlush – o método EndFlush termina uma operação de liberação.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue. EndFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9a283867036254b7a13b45ba152c3f16ecccbdb59d4d59e98c8d1dae7480e13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634216"
---
# <a name="coutputqueueendflush-method"></a>Método COutputQueue. EndFlush

O `EndFlush` método encerra uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
void EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o objeto estiver usando um thread, esse método aguardará o evento [**COutputQueue:: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) . O thread sinaliza esse evento depois de liberar quaisquer amostras pendentes. Se o objeto não estiver usando um thread, esse método chamará o método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) . Em seguida, o `EndFlush` método chama o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




