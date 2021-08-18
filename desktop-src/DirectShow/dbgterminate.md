---
description: A função DbgTerminate limpa a biblioteca de depuração. Ignorado em builds de varejo.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: Função DbgTerminate (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6846f6899730a8b9d128d1bc0a6069fd8a67a5f4f9d8a5a3d618bebad67b0468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821555"
---
# <a name="dbgterminate-function"></a>Função DbgTerminate

A **função DbgTerminate** limpa a biblioteca de depuração. Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Chame essa função se você chamar a [**função DbgInitialise.**](dbginitialise.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 




