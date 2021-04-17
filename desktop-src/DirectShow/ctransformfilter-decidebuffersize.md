---
description: O método DecideBufferSize define os requisitos de buffer do pino de saída.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Método CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752689"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Método CTransformFilter. DecideBufferSize

O `DecideBufferSize` método define os requisitos de buffer do pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) no alocador do pino de saída.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do PIN de entrada downstream.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) do pino de saída chama esse método. A classe derivada deve implementar esse método. Para obter mais informações, consulte [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




