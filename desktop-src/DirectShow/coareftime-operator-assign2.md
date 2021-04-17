---
description: O operador atribui um novo tempo de referência e usa o parâmetro ' RT [REF] '.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = Method (Ctlutil. h)-parâmetro RT [REF]
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
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105775625"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>COARefTime. Operator = Method (Ctlutil. h)-parâmetro RT [REF]

Esse operador atribui um novo tempo de referência.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RT* \[ referência\]
</dt> <dd>

Referência a um valor de [**\_ tempo de referência**](reference-time.md) que especifica o novo tempo de referência em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma referência ao objeto.

## <a name="requirements"></a>Requisitos

| Requisito                    | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Ctlutil. h (incluir fluxos. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




