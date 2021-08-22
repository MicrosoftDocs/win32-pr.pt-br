---
description: O método GetDueCommand recupera um ponteiro para o próximo comando que é devido.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue.GetDueCommand (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e7c8d133537dc2b185c755e65f3a4febbee762c5c2306de37ad0c627434df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016424"
---
# <a name="ccmdqueuegetduecommand-method"></a>Método CCmdQueue.GetDueCommand

O `GetDueCommand` método recupera um ponteiro para o próximo comando que é devido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCmd* 
</dt> <dd>

Endereço de um ponteiro para o comando adiado.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Quantidade de tempo de espera antes de realizar o tempo máximo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará E \_ ABORT se ocorrer um tempo-out. Retornará S \_ OK se for bem-sucedido; caso contrário, retornará um erro. Retorna um objeto que foi incrementado usando **IUnknown::AddRef**.

## <a name="remarks"></a>Comentários

Essa função membro bloqueia até que um comando pendente seja devido. A função membro bloqueia a quantidade de tempo, em milissegundos, especificada no *parâmetro msTimeout.* Os comandos de tempo de fluxo se tornam devidos apenas entre as funções de membro [**CCmdQueue::Run**](ccmdqueue-run.md) e [**CCmdQueue::EndRun.**](ccmdqueue-endrun.md) O comando permanece na fila até ser executado ou cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




