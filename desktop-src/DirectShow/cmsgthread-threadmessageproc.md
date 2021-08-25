---
description: Processa solicitações. Essa é uma função de membro virtual pura.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Método CMsgThread. ThreadMessageProc (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb11a7cac567bd645d0e3fd1c294636b5df9410fbc54012633ec0c0d161b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909696"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>Método CMsgThread. ThreadMessageProc

Processa solicitações. Essa é uma função de membro virtual pura.

## <a name="syntax"></a>Sintaxe


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Código de solicitação.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Parâmetro de sinalizador opcional a ser solicitado.

</dd> <dt>

*lpParam* 
</dt> <dd>

Ponteiro opcional para dados adicionais ou um bloco de dados de retorno.

</dd> <dt>

*pEvent* 
</dt> <dd>

Ponteiro opcional para um objeto de evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Qualquer retorno diferente de zero faz com que o thread saia. Retorna zero, a menos que uma solicitação de saída tenha sido processada recentemente.

## <a name="remarks"></a>Comentários

Essa função virtual pura deve ser substituída em sua classe derivada. Ele será chamado uma vez para cada solicitação em fila por uma chamada para a função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) .

A função membro define os quatro parâmetros. Normalmente, use o parâmetro *uMsg* para indicar a solicitação e os outros três parâmetros serão parâmetros adicionais opcionais. O aplicativo de chamada pode fornecer um ponteiro para um objeto [**CAMEvent**](camevent.md) no parâmetro *pEvent* se o seu aplicativo exigir. Você deve definir esse evento depois de processar o evento usando uma expressão como:


```C++
pEvent->SetEvent
```



Um código de solicitação deve ser reservado para informar ao thread de trabalho para sair. Após o recebimento dessa solicitação, retorne 1 dessa função de membro. Retorne 0 se você não quiser que o thread de trabalho saia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




