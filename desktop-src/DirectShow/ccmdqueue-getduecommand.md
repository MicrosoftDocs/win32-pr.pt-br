---
description: O método GetDueCommand recupera um ponteiro para o próximo comando que é devido.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Método CCmdQueue. GetDueCommand (Winutil. h)
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
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751253"
---
# <a name="ccmdqueuegetduecommand-method"></a>Método CCmdQueue. GetDueCommand

O `GetDueCommand` método recupera um ponteiro para o próximo comando que está vencido.

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

Tempo de espera antes da realização do tempo limite.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ anula se ocorrer um tempo limite. Retornará S \_ OK se for bem-sucedido; caso contrário, retornará um erro. Retorna um objeto que foi incrementado usando **IUnknown:: AddRef**.

## <a name="remarks"></a>Comentários

Essa função de membro é bloqueada até que um comando pendente seja devido. A função de membro é bloqueada para o período de tempo, em milissegundos, especificado no parâmetro *msTimeout* . Os comandos de tempo de transmissão se tornam devido somente às funções de membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) . O comando permanece na fila até ser executado ou cancelado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




