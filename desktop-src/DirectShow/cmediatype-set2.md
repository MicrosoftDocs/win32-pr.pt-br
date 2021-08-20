---
description: O método Set define o tipo de mídia de outro tipo de mídia.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType.Set (Mtype.h) – parâmetro mtype [ref]
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
ms.openlocfilehash: 350e88cefa7c0f5f6946218d220fcad4a118cf53e203a68eeb9f75c0d0eace1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156059"
---
# <a name="cmediatypeset-method-mtypeh"></a>Método CMediaType.Set (Mtype.h)

O `Set` método define o tipo de mídia de outro tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Referência a uma [**estrutura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método copia todo o tipo de mídia do *mtype*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




