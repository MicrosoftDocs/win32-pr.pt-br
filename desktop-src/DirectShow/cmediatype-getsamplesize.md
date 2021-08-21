---
description: O método GetSampleSize recupera o tamanho da amostra.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Método CMediaType.GetSampleSize (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.GetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 120ae54e615e96b368f44c1523703ca35f89d40313f79b450e2cbbd8923829dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156400"
---
# <a name="cmediatypegetsamplesize-method"></a>Método CMediaType.GetSampleSize

O `GetSampleSize` método recupera o tamanho da amostra.

## <a name="syntax"></a>Sintaxe


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o tamanho da amostra for fixo, retornará o tamanho da amostra em bytes. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




