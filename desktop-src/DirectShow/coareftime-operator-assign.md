---
description: Esse operador atribui um novo tempo de referência.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Método COARefTime. Operator = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31784a008a2074156c69abf868739ec27c459dabdba1437397780086d28f9847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084456"
---
# <a name="coareftimeoperator-method-ctlutilh"></a>Método COARefTime. Operator = (Ctlutil. h)

Esse operador atribui um novo tempo de referência.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*área de trabalho* \[ referência\]
</dt> <dd>

Referência a um valor **duplo** que especifica o novo tempo de referência em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




