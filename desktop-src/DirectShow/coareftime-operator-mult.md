---
description: Esse operador multiplica um tempo de referência por um valor.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Método COARefTime. Operator * (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778615"
---
# <a name="coareftimeoperator-method"></a>Método COARefTime. Operator \*

Esse operador multiplica um tempo de referência por um valor.

## <a name="syntax"></a>Sintaxe


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*l* 
</dt> <dd>

Multiplicador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um novo objeto **COARefTime** igual ao produto deste objeto e **l**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COARefTime**](coareftime.md)
</dt> </dl>

 

 




