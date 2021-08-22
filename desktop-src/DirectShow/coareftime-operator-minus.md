---
description: Esse operador subtrai um tempo de referência de outro.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Método COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da8de864f344321cc5dca801782aab1f8476eb91608b42577cca6a34c625e153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073820"
---
# <a name="coareftimeoperator--method"></a>Método COARefTime. Operator

Esse operador subtrai um tempo de referência de outro.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser subtraído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um novo objeto **COARefTime** igual à diferença dos tempos de referência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




