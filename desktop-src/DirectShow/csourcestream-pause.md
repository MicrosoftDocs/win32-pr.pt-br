---
description: O método Pause sinaliza o thread de streaming para se tornar ativo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Método CSourceStream.Pause (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079306"
---
# <a name="csourcestreampause-method"></a>Método CSourceStream.Pause

O `Pause` método sinaliza o thread de streaming para se tornar ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ UNEXPECTED.

## <a name="remarks"></a>Comentários

O [**método CSourceStream::Active**](csourcestream-active.md) chama esse método. Quando o [**método CSourceStream::ThreadProc**](csourcestream-threadproc.md) recebe essa solicitação, ele chama o [**método CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




