---
description: Método COutputQueue. BeginFlush-o método BeginFlush inicia uma operação de liberação.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Método COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099024"
---
# <a name="coutputqueuebeginflush-method"></a>Método COutputQueue. BeginFlush

O `BeginFlush` método inicia uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define a variável de membro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) como **true**. Se o objeto estiver usando um thread, o thread chamará o método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) para liberar quaisquer amostras pendentes. Caso contrário, o objeto chamará **FreeSamples** durante o método [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) . Esse método também define a variável de membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) como S \_ false, o que faz com que o objeto descarte todas as novas amostras.

O objeto passa o downstream de notificação de liberação chamando o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




