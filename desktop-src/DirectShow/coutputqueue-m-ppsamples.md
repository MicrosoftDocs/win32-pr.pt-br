---
description: Matriz de exemplos de tamanho COutputQueue::m \_ lBatchSize.
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: Membro COutputQueue::m_ppSamples (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103146"
---
# <a name="coutputqueuem_ppsamples-member"></a>Membro COutputQueue::m \_ ppSamples

Matriz de exemplos de tamanho [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintaxe


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Comentários

O thread de trabalho recebe amostras da fila e as coloca nessa matriz. Ele passa a matriz para o [**método IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) Se o objeto não estiver usando um thread de trabalho, o objeto coloca amostras diretamente nessa matriz. A [**variável membro COutputQueue::m \_ List**](coutputqueue-m-list.md) contém a fila.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




