---
description: O operador atribui um novo tempo de referência e usa o parâmetro 'rt [ref]'.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Método COARefTime.operator= (Ctlutil.h) – parâmetro rt [ref]
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
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103156"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>Método COARefTime.operator= (Ctlutil.h) – parâmetro rt [ref]

Esse operador atribui um novo tempo de referência.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referência a um [**valor \_ REFERENCE TIME**](reference-time.md) que especifica o novo tempo de referência em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto .

## <a name="requirements"></a>Requisitos

| Requisito                    | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Ctlutil.h (incluir Fluxos.h)                                                                                   |
| Biblioteca | Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




