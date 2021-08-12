---
description: Define o valor de tempo-máximo de depuração. Ignorado em builds de varejo.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Função DbgSetWaitTimeout (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a5522184b9e88cd4b8ac9f23246f96c13ffad2175d625334de32d34c750e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654018"
---
# <a name="dbgsetwaittimeout-function"></a>Função DbgSetWaitTimeout

Define o valor de tempo-máximo de depuração. Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dwtimeout* 
</dt> <dd>

Valor de tempo-out em milissegundos ou INFINITE para aguardar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Em builds de depuração, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usam esse valor como o intervalo de tempo-out.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de depuração de espera](wait-debugging-functions.md)
</dt> </dl>

 

 




