---
description: O método GetRequest aguarda a próxima solicitação de thread.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Método CSourceStream.GetRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e28a8e57535a49903cd2a7b23fb0d0d179bf910b20225042c65b3bdcda620f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073200"
---
# <a name="csourcestreamgetrequest-method"></a>Método CSourceStream.GetRequest

O `GetRequest` método aguarda a próxima solicitação de thread.

## <a name="syntax"></a>Sintaxe


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a próxima solicitação de thread.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CAMThread::GetRequest.**](camthread-getrequest.md) O valor de retorno é lançado para o seguinte tipo enumerado:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




