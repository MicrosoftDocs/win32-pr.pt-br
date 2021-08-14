---
description: A função IsEqualObject verifica se duas interfaces estão no mesmo objeto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Função IsEqualObject (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817445"
---
# <a name="isequalobject-function"></a>Função IsEqualObject

A `IsEqualObject` função verifica se duas interfaces estão no mesmo objeto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFirst* 
</dt> <dd>

Ponteiro para uma interface.

</dd> <dt>

*pSecond* 
</dt> <dd>

Ponteiro para a outra interface.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se as interfaces estão no mesmo objeto ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




