---
description: O método ThreadProc recupera amostras da fila e as entrega ao PIN de entrada.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Método COutputQueue. ThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749246"
---
# <a name="coutputqueuethreadproc-method"></a>Método COutputQueue. ThreadProc

O `ThreadProc` método recupera amostras da fila e as entrega ao PIN de entrada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna zero.

## <a name="remarks"></a>Comentários

O método [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md) chama esse método, que implementa o loop de thread principal. Dentro do loop, o método executa as seguintes etapas:

1.  Recupera um exemplo para a fila.
2.  Se o exemplo for uma mensagem de controle, o Thread executará a ação de controle. Caso contrário, ele coloca o exemplo na matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) .
3.  Quando a matriz estiver cheia (ou se [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) for **false**), o thread chamará o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) para entregar os exemplos.
4.  Se nenhuma amostra for enfileirada, o thread aguardará o semáforo [**COutputQueue:: m \_ hSem**](coutputqueue-m-hsem.md) .

O thread termina quando a variável de membro [**COutputQueue:: m \_ bTerminate**](coutputqueue-m-bterminate.md) se torna **verdadeira**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




