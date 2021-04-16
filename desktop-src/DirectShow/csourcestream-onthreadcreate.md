---
description: O método OnThreadCreate é chamado quando o thread de streaming é inicializado.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Método CSourceStream. OnThreadCreate (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750654"
---
# <a name="csourcestreamonthreadcreate-method"></a>Método CSourceStream. OnThreadCreate

O `OnThreadCreate` método é chamado quando o thread de streaming é inicializado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O procedimento de thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chama esse método quando recebe pela primeira vez uma solicitação [**CSourceStream:: init**](csourcestream-init.md) . O método não faz nada na classe base. A classe derivada pode substituir esse método para executar inicializações de thread. Se a classe derivada retornar um código de erro, o thread será encerrado com um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




