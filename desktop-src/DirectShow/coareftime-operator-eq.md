---
description: Esse operador testa a igualdade entre dois tempos de referência.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Método COARefTime.operator== (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36951e2a2d0f82d73106f5b78ef9eb7e0b067c34dc4db3fd72521f48d8d4beb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831816"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator==

Esse operador testa a igualdade entre dois tempos de referência.

## <a name="syntax"></a>Sintaxe


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser comparado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se os dois objetos são iguais. Caso contrário, **retornará FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




