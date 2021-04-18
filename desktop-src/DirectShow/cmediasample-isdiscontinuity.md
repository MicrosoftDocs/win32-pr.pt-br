---
description: 'O método IsDiscontinuity determina se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método IMediaSample:: IsDiscontinuity.'
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: Método CMediaSample. IsDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755349"
---
# <a name="cmediasampleisdiscontinuity-method"></a>Método CMediaSample. IsDiscontinuity

O `IsDiscontinuity` método determina se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método [**IMediaSample:: IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o exemplo for uma interrupção no fluxo de dados e, \_ caso contrário, false.

## <a name="remarks"></a>Comentários

A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




