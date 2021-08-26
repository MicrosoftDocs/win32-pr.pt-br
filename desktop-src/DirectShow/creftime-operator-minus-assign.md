---
description: O operador -= subtrai uma hora de referência de outra.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: Método CRefTime.operator-= (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 854831c2ed9cf5b636160dccaf002a7ea9ac37ebaa5e970f8b63dd3f112cdda6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108036"
---
# <a name="creftimeoperator--method"></a>Método CRefTime.operator-=

O operador -= subtrai uma hora de referência de outra.

## <a name="syntax"></a>Sintaxe


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referência a um **objeto CRefTime.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Reftime.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




