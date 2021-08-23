---
description: O método CMediaType.Set (Mtype.h) define o tipo de mídia de outro tipo de mídia. O método usa o parâmetro 'cmtype'.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Método CMediaType.Set (Mtype.h) – parâmetro cmtype [ref]
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585876"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Método CMediaType.Set (Mtype.h) – parâmetro cmtype [ref]

O `Set` método define o tipo de mídia de outro tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Referência a um [**objeto CMediaType.**](cmediatype.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método copia todo o tipo de mídia do *cmtype*.

## <a name="requirements"></a>Requisitos

| Requisito                   | Valor                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro  | Mtype.h (incluir Fluxos.h)                                                                                     |
| Biblioteca | Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




