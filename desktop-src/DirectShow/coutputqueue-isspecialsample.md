---
description: O método IsSpecialSample determina se os dados em fila são uma mensagem de controle.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Método COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c192196869f86e8d78da2f6b38a661373e115753d99e554f4b7a868eb0b484fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688216"
---
# <a name="coutputqueueisspecialsample-method"></a>Método COutputQueue. IsSpecialSample

O `IsSpecialSample` método determina se os dados em fila são uma mensagem de controle.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para um item na fila.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se *pSample* for uma mensagem de controle ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O método [**COutputQueue:: QueueSample**](coutputqueue-queuesample.md) pode receber mensagens de controle além dos exemplos de mídia. Uma mensagem de controle é uma constante definida (conversão para um \_ tipo PTR longo) que instrui o thread a executar uma ação. As mensagens de controle não contêm dados de mídia. Para obter mais informações, consulte **COutputQueue:: QueueSample**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




