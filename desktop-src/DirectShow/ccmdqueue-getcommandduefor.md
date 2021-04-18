---
description: O método GetCommandDueFor recupera um comando adiado que é agendado em um horário especificado.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Método CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785369"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>Método CCmdQueue. GetCommandDueFor

O `GetCommandDueFor` método recupera um comando adiado que é agendado em um horário especificado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStream* 
</dt> <dd>

Hora em que o comando está agendado.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Endereço de um ponteiro para o comando adiado a ser executado no momento especificado no parâmetro *tStream* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna VFW \_ E \_ não \_ encontrado se nenhum comando for devido; caso contrário, retornará S \_ OK.

## <a name="remarks"></a>Comentários

Essa função de membro usa um fluxo de tempo e retorna o comando adiado agendado nesse momento. O deslocamento real do tempo de transmissão é calculado quando a fila de comandos é executada. Os comandos permanecem na fila até serem executados ou cancelados. Esta função de membro não será bloqueada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




