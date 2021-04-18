---
description: 'O método GetSize recupera o tamanho do buffer. Esse método implementa o método IMediaSample:: GetSize.'
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: Método CMediaSample. GetSize (Amfilter. h)
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
ms.openlocfilehash: ff4146b66ca62905fe54eeb88d1e38ccf56ceea9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757702"
---
# <a name="cmediasamplegetsize-method"></a>Método CMediaSample. GetSize

O `GetSize` método recupera o tamanho do buffer. Esse método implementa o método [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) .

## <a name="syntax"></a>Sintaxe


```C++
LONG GetSize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o tamanho do buffer, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




