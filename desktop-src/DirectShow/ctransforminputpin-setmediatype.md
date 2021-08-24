---
description: Método CTransformInputPin.SetMediaType – o método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Método CTransformInputPin.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9343f464a7a5abe19c9310ffc7b36e504c02b23abf6b0f88d822815ae9952daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767566"
---
# <a name="ctransforminputpinsetmediatype-method"></a>Método CTransformInputPin.SetMediaType

O `SetMediaType` método define o tipo de mídia para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mt* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBasePin::SetMediaType.**](cbasepin-setmediatype.md) Ele chama o método [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) do filtro para informar o filtro.

O pino deve verificar se o tipo de mídia é aceitável antes de chamar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




