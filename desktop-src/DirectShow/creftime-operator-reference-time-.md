---
description: O \_ operador tempo de referência () converte o objeto em um tipo de dados de tempo de referência \_ .
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método CReftime. Operator REFERENCE_TIME (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775620"
---
# <a name="creftimeoperator-reference_time-method"></a>Método de tempo de referência CReftime. Operator \_

O `REFERENCE_TIME()` operador converte o objeto em um tipo de dados de [**\_ tempo de referência**](reference-time.md) .

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o valor de [**CRefTime:: m \_ time**](creftime-m-time.md).

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como usar esse operador cast:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>REFTIME. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




