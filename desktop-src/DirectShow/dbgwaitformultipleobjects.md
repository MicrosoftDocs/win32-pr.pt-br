---
description: Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Função DbgWaitForMultipleObjects (Wxdebug. h)
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
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751672"
---
# <a name="dbgwaitformultipleobjects-function"></a>Função DbgWaitForMultipleObjects

Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados.

Em uma compilação de depuração, essa função acionará uma declaração se o intervalo de tempo limite expirar antes que os objetos sejam sinalizados. Para definir o intervalo de tempo limite, chame a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .

Em uma compilação de varejo, essa função é equivalente à função **WaitForMultipleObjects** com um intervalo de tempo limite de infinito.

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

*nCount* 
</dt> <dd>

Número de objetos.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Matriz de identificadores para objetos, de tamanho *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Valor booliano que especifica se deve aguardar todos os objetos. Se **for true**, a função aguardará que todos os objetos sejam sinalizados. Caso contrário, ele aguarda pelo menos um objeto a ser sinalizado.

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

 

 




