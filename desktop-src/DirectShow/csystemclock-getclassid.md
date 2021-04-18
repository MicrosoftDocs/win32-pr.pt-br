---
description: 'O método GetClassID recupera o identificador de classe (CLSID) do objeto. Esse método implementa o método IPersist:: GetClassID.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Método CSystemClock. GetClassID (Sysclock. h)
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
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749828"
---
# <a name="csystemclockgetclassid-method"></a>Método CSystemClock. GetClassID

O `GetClassID` método recupera o identificador de classe (CLSID) do objeto. Esse método implementa o método **IPersist:: GetClassID** .

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

Ponteiro para uma variável que recebe o valor CLSID \_ SystemClock.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Classe CSystemClock<br/>                                                                                                                                                              |
| parâmetro<br/>  | <dl> <dt>Sysclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




