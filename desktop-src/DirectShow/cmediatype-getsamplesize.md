---
description: O método getamostrate recupera o tamanho da amostra.
ms.assetid: 5cc98556-cca6-46ca-ad33-cd40011ff6f4
title: Método CMediaType. getsampleize (mtype. h)
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
ms.openlocfilehash: cc5b80e20ad2a16af9c25c68499348ffa744c0fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769227"
---
# <a name="cmediatypegetsamplesize-method"></a>Método CMediaType. getsampleize

O `GetSampleSize` método recupera o tamanho da amostra.

## <a name="syntax"></a>Sintaxe


```C++
ULONG GetSampleSize() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se o tamanho da amostra for fixo, o retornará o tamanho da amostra em bytes. Caso contrário, retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




