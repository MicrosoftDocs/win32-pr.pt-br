---
description: Método CTransformFilter. DecideBufferSize – o método DecideBufferSize define os requisitos de buffer do pino de saída.
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
ms.openlocfilehash: 1a1aba3ec43318079a73f0c94c8446b637ece29a5b61752462eeb8fc5898f5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907696"
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

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

O método [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) do pino de saída chama esse método. A classe derivada deve implementar esse método. Para obter mais informações, consulte [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




