---
description: Esse operador testa se um tempo de referência é maior ou igual a outro.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: COARefTime. Operator<= método (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 448f36a9c746c22878d8bb0e48028dff211962cbf49827eab3c14f2b4af6b38c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087276"
---
# <a name="coareftimeoperator-method"></a>COARefTime. Operator<= método

Esse operador testa se um tempo de referência é maior ou igual a outro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser comparado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se esse objeto for maior ou igual a *RT*. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




