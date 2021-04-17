---
description: A função isequalobject verifica se duas interfaces estão no mesmo objeto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Função isequalobject (Wxutil. h)
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
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784021"
---
# <a name="isequalobject-function"></a>Função isequalobject

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

## <a name="return-value"></a>Retornar valor

Retornará **true** se as interfaces estiverem no mesmo objeto ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




