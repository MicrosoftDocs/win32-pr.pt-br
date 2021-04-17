---
description: Aguarda a um objeto ser sinalizado.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Função DbgWaitForSingleObject (Wxdebug. h)
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
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812784"
---
# <a name="dbgwaitforsingleobject-function"></a>Função DbgWaitForSingleObject

Aguarda a um objeto ser sinalizado.

Em uma compilação de depuração, essa função acionará uma declaração se o intervalo de tempo limite expirar antes de o objeto ser sinalizado. Para definir o intervalo de tempo limite, chame a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

Em uma compilação de varejo, essa função é equivalente à função **WaitForSingleObject** com um intervalo de tempo limite de infinito.

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

Identificador para o objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aguardar funções de depuração](wait-debugging-functions.md)
</dt> </dl>

 

 




