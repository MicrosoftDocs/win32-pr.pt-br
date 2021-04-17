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
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789965"
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

## <a name="return-value"></a>Retornar valor

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




