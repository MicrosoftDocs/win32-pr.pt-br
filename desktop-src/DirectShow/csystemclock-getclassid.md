---
description: O método GetClassID recupera o CLSID (identificador de classe) do objeto . Esse método implementa o método IPersist::GetClassID.
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Método CSystemClock.GetClassID (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2afb141c3a79255504eb13dadb39cc0fb5094c19e0979db04c251f1e2fe75133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317186"
---
# <a name="csystemclockgetclassid-method"></a>Método CSystemClock.GetClassID

O `GetClassID` método recupera o CLSID (identificador de classe) do objeto . Esse método implementa o **método IPersist::GetClassID.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pclsid* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor CLSID \_ SystemClock.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| parâmetro<br/>  | <dl> <dt>Sysclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




