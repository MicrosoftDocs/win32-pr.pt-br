---
description: Construtor de COutputQueue. COutputQueue-método de construtor.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Construtor COutputQueue. COutputQueue (Outputq. h)
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
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095324"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Construtor COutputQueue. COutputQueue

Método de construtor.

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

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada. O objeto fornecerá amostras para esse PIN.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um código de retorno **HRESULT** . Defina o valor como S \_ OK antes de chamar esse método. No retorno, *PHR* recebe um valor que indica o êxito ou a falha do método.

</dd> <dt>

*bAuto* 
</dt> <dd>

Sinalizador que especifica se o objeto decide quando criar uma fila. Se **for true**, o objeto criará uma fila somente se o PIN de entrada puder ser bloqueado. Se **for false**, o parâmetro *bQueue* especificará se uma fila deve ser criada.

</dd> <dt>

*bQueue* 
</dt> <dd>

Se *Bauto* for **true**, esse parâmetro será ignorado. Se *Bauto* for **false**, esse sinalizador especificará se uma fila deve ser criada.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Número máximo de amostras a serem entregues em um lote.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Sinalizador que especifica se os tamanhos de lote exatos devem ser usados. Se **for true**, o objeto aguardará exemplos de *lBatchSize* antes de entregá-los ao PIN de entrada. Se **for false**, o objeto fornecerá exemplos à medida que ele os receber.

</dd> <dt>

*lListSize* 
</dt> <dd>

Tamanho do cache da fila. O valor padrão, defaultcache, é uma constante definida para a classe [**CBaseList**](cbaselist.md) .

</dd> <dt>

*dwPriority* 
</dt> <dd>

Prioridade do thread que fornece exemplos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se *Bauto* for **true**, o objeto chamará o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) no PIN do downstream. Se **ReceiveCanBlock** retornar S \_ OK (o que significa que o PIN pode bloquear em [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), o objeto criará um thread para fornecer exemplos. Caso contrário, ele não cria um thread.

Se *Bauto* for **false**, o valor de *bQueue* determinará se um thread deve ser criado.

Se o objeto criar um thread, ele atribuirá o identificador de thread à variável de membro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) . O procedimento de thread é [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)e o parâmetro thread é um ponteiro para isso. O objeto também cria uma fila para manter amostras, que é fornecida pela variável de membro da [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




