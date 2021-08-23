---
description: Esse operador adiciona dois tempos de referência e define esse objeto como o resultado.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Método COARefTime.operator+= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dcb635e3026cec18aa5bea199b6712c15c6472d81e9b6707267d15d7afcfa6ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585556"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime.operator+=

Esse operador adiciona dois tempos de referência e define esse objeto como o resultado.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referência ao objeto **COARefTime** a ser acrescentado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




