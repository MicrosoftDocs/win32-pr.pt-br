---
description: O método set define o tipo de mídia de outro tipo de mídia.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType. Set (mtype. h)
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
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756594"
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

 

 




