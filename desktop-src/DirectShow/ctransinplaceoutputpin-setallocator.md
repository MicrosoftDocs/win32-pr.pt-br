---
description: O método SetAllocator especifica um alocador para a conexão.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Método CTransInPlaceOutputPin.SetAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 568a95df0d0cee39245c268fa1c49505531ddc84e1fd1542a1eae170e5c7d0da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053176"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>Método CTransInPlaceOutputPin.SetAllocator

O `SetAllocator` método especifica um alocador para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator do**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) alocador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O pino de saída para esse filtro nunca fornece um alocador. Esse método especifica o alocador para o pino de saída. Ele define o valor da variável de membro [**CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




