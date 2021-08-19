---
description: Esse operador adiciona dois tempos de referência.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Método COARefTime. Operator + (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348151b4bb7dc7cca6578755e10934364ba59b8ac5447c0bce4b5240483e7fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954335"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime. Operator +

Esse operador adiciona dois tempos de referência.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um novo objeto **COARefTime** igual à soma dos tempos de referência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




