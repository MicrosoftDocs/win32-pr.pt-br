---
description: 'O método SetPreroll especifica se este exemplo é uma amostra de preversão. Um exemplo de preroll não deve ser exibido. Esse método implementa o método IMediaSample:: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754262"
---
# <a name="cmediasamplesetpreroll-method"></a>Método CMediaSample. SetPreroll

O `SetPreroll` método especifica se este exemplo é uma amostra de preversão. Um exemplo de preroll não deve ser exibido. Esse método implementa o método [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Valor booliano que especifica se este é um exemplo de preversão. Se for **verdadeiro**, este é um exemplo de preversão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica a propriedade de preversão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




