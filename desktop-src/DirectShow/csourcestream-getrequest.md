---
description: O método GetRequest aguarda a próxima solicitação de thread.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Método CSourceStream. GetRequest (origem. h)
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
ms.openlocfilehash: 3f45e6f6cf269f7aca6741d8e1c150c7054b07f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748802"
---
# <a name="csourcestreamgetrequest-method"></a>Método CSourceStream. GetRequest

O `GetRequest` método aguarda a próxima solicitação de thread.

## <a name="syntax"></a>Sintaxe


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a próxima solicitação de thread.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CAMThread:: GetRequest**](camthread-getrequest.md) . O valor de retorno é convertido para o seguinte tipo enumerado:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




