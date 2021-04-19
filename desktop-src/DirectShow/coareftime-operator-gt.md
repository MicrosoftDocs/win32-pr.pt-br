---
description: Esse operador testa se um tempo de referência é maior que o outro.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Método de>. Operator COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756618"
---
# <a name="coareftimeoperator-method"></a>Método de>. Operator COARefTime

Esse operador testa se um tempo de referência é maior que o outro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser comparado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se esse objeto for estritamente maior que *RT*. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




