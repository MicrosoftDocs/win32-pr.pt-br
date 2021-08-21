---
description: O método GetSize recupera o tamanho do buffer. Esse método implementa o método IMediaSample::GetSize.
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Método CMediaSample.GetSize (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3559f972f35a01738c60f32414ab0b42a079032ac5bc6b3ab0e5b7212900d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156747"
---
# <a name="cmediasamplegetsize-method"></a>Método CMediaSample.GetSize

O `GetSize` método recupera o tamanho do buffer. Esse método implementa o [**método IMediaSample::GetSize.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)

## <a name="syntax"></a>Sintaxe


```C++
LONG GetSize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o tamanho do buffer, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




