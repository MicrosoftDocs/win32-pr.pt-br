---
description: Recupera um objeto CMsg enfileirado que contém uma solicitação.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Método CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770092"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>Método CMsgThread. GetThreadMsg

Recupera um objeto [**CMsg**](cmsg.md) enfileirado que contém uma solicitação.

## <a name="syntax"></a>Sintaxe


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*msg* 
</dt> <dd>

Ponteiro para um objeto [**CMsg**](cmsg.md) alocado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro é chamada da função [**ThreadProc**](camthread-threadproc.md) privada do thread de trabalho para recuperar a próxima função de membro. O parâmetro *msg* deve apontar para um objeto [**CMsg**](cmsg.md) alocado que será preenchido com os parâmetros para a próxima solicitação na fila. Se não houver nenhuma solicitação em fila, essa função de membro será bloqueada até que a próxima solicitação seja enfileirada (por uma chamada para a função de membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




