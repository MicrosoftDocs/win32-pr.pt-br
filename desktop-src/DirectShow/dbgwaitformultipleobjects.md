---
description: Aguarda que qualquer (ou todos) dos objetos especificados seja sinalizado.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Função DbgWaitForMultipleObjects (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acab4a7f59fe0775e8e474f8a8a2342a5f29ae6266ee36432b0fc1b0e597141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654056"
---
# <a name="dbgwaitformultipleobjects-function"></a>Função DbgWaitForMultipleObjects

Aguarda que qualquer (ou todos) dos objetos especificados seja sinalizado.

Em um build de depuração, essa função dispara uma declaração se o intervalo de tempo-expirar antes que os objetos sejam sinalados. Para definir o intervalo de tempo-out, chame a [**função DbgSetWaitTimeout.**](dbgsetwaittimeout.md)

Em um build de varejo, essa função é equivalente à **função WaitForMultipleObjects** com um intervalo de tempo-tempo de INFINITE.

## <a name="syntax"></a>Sintaxe


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ncount* 
</dt> <dd>

Número de objetos.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Matriz de alças para objetos, de tamanho *nCount.*

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valor booliana que especifica se é preciso aguardar todos os objetos. Se **TRUE**, a função aguardará a sinalização de todos os objetos. Caso contrário, ele aguardará pelo menos um objeto ser sinalizado.

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

 

 




