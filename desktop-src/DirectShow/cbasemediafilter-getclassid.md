---
description: O método GetClassID recupera o identificador de classe. Esse método implementa o método IPersist::GetClassID.
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Método CBaseMediaFilter.GetClassID (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a733c3ef6e7098a556facb5258f567bdae0179ba4da133076b9bbc961cf0b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502916"
---
# <a name="cbasemediafiltergetclassid-method"></a>Método CBaseMediaFilter.GetClassID

O `GetClassID` método recupera o identificador de classe. Esse método implementa o **método IPersist::GetClassID.**

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

Ponteiro para uma variável que recebe o identificador de classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




