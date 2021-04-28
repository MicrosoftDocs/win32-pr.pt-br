---
description: Método CTransformOutputPin. SetMediaType – o método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Método CTransformOutputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084794"
---
# <a name="ctransformoutputpinsetmediatype-method"></a>Método CTransformOutputPin. SetMediaType

O `SetMediaType` método define o tipo de mídia para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) . Ele chama o método [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) do filtro para informar o filtro.

O PIN deve verificar se o tipo de mídia é aceitável antes de chamar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




