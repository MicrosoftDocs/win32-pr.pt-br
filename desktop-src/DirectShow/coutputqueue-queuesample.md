---
description: O método QueueSample enfileira um exemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue.QueueSample (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909586"
---
# <a name="coutputqueuequeuesample-method"></a>Método COutputQueue.QueueSample

O `QueueSample` método enfilfilia um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample do**](/windows/desktop/api/Strmif/nn-strmif-imediasample) exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método adiciona um exemplo à parte final da fila. Mantenha a seção crítica antes de chamar esse método e chame-a somente quando o objeto estiver usando um thread para fornecer exemplos. Para determinar se o objeto está usando um thread, chame o [**método COutputQueue::IsQueued.**](coutputqueue-isqueued.md)

Esse método também pode ser usado para colocar mensagens de controle na fila. Uma mensagem de controle é uma constante definida (cast em um tipo PTR LONG) que instrui o thread a \_ executar alguma ação. A **classe COutputQueue** define as mensagens de controle mostradas na tabela a seguir.



| Rótulo | Valor |
|---------------|----------------------------------------|
| Mensagem       | Ação                                 |
| PACOTE \_ EOS   | Entregar uma notificação de fim de fluxo. |
| NOVO \_ SEGMENTO  | Entregar um novo segmento.                 |
| REDEFINIR \_ PACOTE | Redefina o estado da fila.          |
| ENVIAR \_ PACOTE  | Enviar um lote parcial de exemplos.       |



 

Esse é um método protegido, que a **classe COutputQueue** usa internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




