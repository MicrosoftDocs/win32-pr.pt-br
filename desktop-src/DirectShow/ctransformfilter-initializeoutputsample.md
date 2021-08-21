---
description: O método InitializeOutputSample recupera um novo exemplo de saída e inicializa-o.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Inimétodo tializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 083867f2ef6b2e40462112036dbbb000c25bc3ad2bb443f011235e36bf245ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953615"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.Inimétodo tializeOutputSample

O `InitializeOutputSample` método recupera um novo exemplo de saída e inicializa-o.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de entrada.

</dd> <dt>

*ppOutSample* 
</dt> <dd>

Recebe um ponteiro para a interface **IMediaSample** da amostra de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado pelo método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) para preparar o exemplo de saída. Em geral, você não precisa chamar esse método em sua classe derivada, a menos que substitua o método **Receive** .

Esse método recupera uma nova amostra do alocador do pino de saída. Em seguida, ele copia as propriedades de exemplo do exemplo de entrada para o exemplo de saída. As propriedades de exemplo são definidas na estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




