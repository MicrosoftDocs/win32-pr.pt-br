---
description: O método set define o tipo de mídia de outro tipo de mídia.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType. Set (mtype. h)-parâmetro mtype [REF]
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389084"
---
# <a name="cmediatypeset-method-mtypeh"></a>Método CMediaType. Set (mtype. h)

O `Set` método define o tipo de mídia de outro tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtype* \[ referência\]
</dt> <dd>

Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método copia todo o tipo de mídia de *mtype*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




