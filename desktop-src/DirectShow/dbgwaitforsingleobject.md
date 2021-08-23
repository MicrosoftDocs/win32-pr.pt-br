---
description: Aguarda até que um objeto seja sinalizado.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Função DbgWaitForSingleObject (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749346"
---
# <a name="dbgwaitforsingleobject-function"></a>Função DbgWaitForSingleObject

Aguarda até que um objeto seja sinalizado.

Em um build de depuração, essa função dispara uma declaração se o intervalo de tempo-expirar antes que o objeto seja sinalizado. Para definir o intervalo de tempo-out, chame a [**função DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

Em um build de varejo, essa função é equivalente à **função WaitForSingleObject** com um intervalo de tempo-tempo de INFINITE.

## <a name="syntax"></a>Sintaxe


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*h* 
</dt> <dd>

Identificador para o objeto .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de depuração de espera](wait-debugging-functions.md)
</dt> </dl>

 

 




