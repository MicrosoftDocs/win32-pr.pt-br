---
description: 'O método SetDiscontinuity especifica se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método IMediaSample:: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Método CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810248"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Método CMediaSample. SetDiscontinuity

O `SetDiscontinuity` método especifica se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valor booliano que especifica se este exemplo é uma descontinuidade. Se **for true**, o exemplo de mídia será descontínuo com o exemplo anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica a propriedade de descontinuidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




