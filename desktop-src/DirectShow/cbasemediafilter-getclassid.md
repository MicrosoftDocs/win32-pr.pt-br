---
description: 'O método GetClassID recupera o identificador de classe. Esse método implementa o método IPersist:: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Método CBaseMediaFilter. GetClassID (Amfilter. h)
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
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748226"
---
# <a name="cbasemediafiltergetclassid-method"></a>Método CBaseMediaFilter. GetClassID

O `GetClassID` método recupera o identificador de classe. Esse método implementa o método **IPersist:: GetClassID** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClsID* 
</dt> <dd>

Ponteiro para uma variável que recebe o identificador de classe.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




