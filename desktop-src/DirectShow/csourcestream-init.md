---
description: O método Init inicializa o thread de streaming.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: CSourceStream.Init (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e656ba46b25045406fb794653078b72e2c47155635cf24ae4a99b35238aa51df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871306"
---
# <a name="csourcestreaminit-method"></a>CSourceStream.Init

O `Init` método inicializa o thread de streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Init();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT.**

## <a name="remarks"></a>Comentários

Esse método deve ser a primeira solicitação de thread enviada para o [**método CSourceStream::ThreadProc.**](csourcestream-threadproc.md) O [**método CSourceStream::Active**](csourcestream-active.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




