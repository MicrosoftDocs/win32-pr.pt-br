---
description: O operador = atribui um novo tempo de referência.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Método CRefTime.operator= (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4fe9a8f6f40dd1d0a7b0e38339c3ab21c44a989648e6c032b17a0ed3ac3b4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108066"
---
# <a name="creftimeoperator-method-reftimeh"></a>Método CRefTime.operator= (Reftime.h)

O operador = atribui um novo tempo de referência.

## <a name="syntax"></a>Sintaxe


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referência a um **objeto CRefTime** que especifica a nova hora de referência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma referência ao objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Reftime.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




