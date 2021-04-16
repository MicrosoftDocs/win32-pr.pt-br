---
description: Esse operador testa se um tempo de referência é menor que o outro.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Método de<. Operator COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758852"
---
# <a name="coareftimeoperator-method"></a>Método de<. Operator COARefTime

Esse operador testa se um tempo de referência é menor que o outro.

## <a name="syntax"></a>Sintaxe


```C++
BOOL operator<(
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

Retornará **true** se esse objeto for estritamente menor que *RT*. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




