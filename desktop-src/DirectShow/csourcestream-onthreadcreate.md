---
description: O método OnThreadCreate é chamado quando o thread de streaming é inicializado.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Método CSourceStream.OnThreadCreate (Source.h)
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
ms.openlocfilehash: 6e263f0ae72838504ab6d219c71d7841291a3edd2a7d6b719d112c74fb30c23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907706"
---
# <a name="csourcestreamonthreadcreate-method"></a>Método CSourceStream.OnThreadCreate

O `OnThreadCreate` método é chamado quando o thread de streaming é inicializado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O procedimento de thread, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), chama esse método quando recebe pela primeira vez uma [**solicitação CSourceStream::Init.**](csourcestream-init.md) O método não faz nada na classe base. A classe derivada pode substituir esse método para executar inicializações de thread. Se a classe derivada retornar um código de erro, o thread será final com um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




