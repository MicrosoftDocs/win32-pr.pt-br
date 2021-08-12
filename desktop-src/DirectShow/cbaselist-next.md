---
description: O método Next recupera a próxima posição na lista.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Método CBaseList.Next (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d07030c046f3fe55178707af297542f383bfd5cf75f40169b5c93cfafa1c698b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658952"
---
# <a name="cbaselistnext-method"></a>Método CBaseList.Next

O `Next` método recupera a próxima posição na lista.

## <a name="syntax"></a>Sintaxe


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor POSITION.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o indicador de posição que segue a posição especificada por *pos.*

## <a name="remarks"></a>Comentários

Se *pos* for a última posição na lista, o método retornará **NULL.** Se *pos* for **NULL,** o método retornará a primeira posição na lista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




