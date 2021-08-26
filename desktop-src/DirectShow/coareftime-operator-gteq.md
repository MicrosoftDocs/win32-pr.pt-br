---
description: Esse operador testa se uma hora de referência é menor ou igual a outra.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: MÉTODO COARefTime.operator>= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6d19686fc2c904534f66882172db6bec52b4873a36104ce78d2d826a771978d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108466"
---
# <a name="coareftimeoperator-method"></a>MÉTODO COARefTime.operator>=

Esse operador testa se uma hora de referência é menor ou igual a outra.

## <a name="syntax"></a>Sintaxe


```C++
BOOL operator>=(
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

Retornará **TRUE** se esse objeto for menor ou igual a *rt*. Caso contrário, **retornará FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




