---
description: Construtor COutputQueue.COutputQueue – Método do construtor.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Construtor COutputQueue.COutputQueue (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bf50314fd0ceb1afbe00c5a6a63708cc79ab38d77931c80b086039c7ca9704c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087236"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Construtor COutputQueue.COutputQueue

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInputPin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada. O objeto fornecerá exemplos para esse pino.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **código de retorno HRESULT.** De definir o valor como S \_ OK antes de chamar esse método. No retorno, *phr* recebe um valor que indica o êxito ou a falha do método.

</dd> <dt>

*bAuto* 
</dt> <dd>

Sinalizador que especifica se o objeto decide quando criar uma fila. Se **TRUE**, o objeto criará uma fila somente se o pino de entrada for bloqueado. Se **FALSE**, o *parâmetro bQueue* especifica se uma fila deve ser criado.

</dd> <dt>

*bQueue* 
</dt> <dd>

Se *bAuto* for **TRUE,** esse parâmetro será ignorado. Se *bAuto* for **FALSE,** esse sinalizador especificará se uma fila deve ser criado.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Número máximo de amostras a entregar em um lote.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Sinalizador que especifica se é preciso usar tamanhos de lote exatos. Se **TRUE**, o objeto aguardará amostras *de lBatchSize* antes de entregar para o pino de entrada. Se **FALSE**, o objeto entregará amostras conforme ele as recebe.

</dd> <dt>

*lListSize* 
</dt> <dd>

Tamanho do cache para a fila. O valor padrão, DEFAULTCACHE, é uma constante definida para a [**classe CBaseList.**](cbaselist.md)

</dd> <dt>

*dwPriority* 
</dt> <dd>

Prioridade do thread que fornece exemplos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se *bAuto* for **TRUE,** o objeto chamará o [**método IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) no pino downstream. Se **ReceiveCanBlock** retornar S OK (o que significa que o pino pode bloquear em chamadas \_ [**IMemInputPin::Receive),**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) o objeto criará um thread para fornecer exemplos. Caso contrário, ele não criará um thread.

Se *bAuto* for **FALSE,** o valor *de bQueue* determinará se um thread deve ser criado.

Se o objeto criar um thread, ele atribuirá o identificador de thread à variável de membro [**COutputQueue::m \_ hThread.**](coutputqueue-m-hthread.md) O procedimento de thread [**é COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md)e o parâmetro thread é um ponteiro para isso. O objeto também cria uma fila para manter amostras, que é determinada pela variável membro [**COutputQueue::m \_ List.**](coutputqueue-m-list.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




