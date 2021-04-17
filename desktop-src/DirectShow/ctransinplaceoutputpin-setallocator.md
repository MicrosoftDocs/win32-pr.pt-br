---
description: O método setalocador especifica um alocador para a conexão.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Método CTransInPlaceOutputPin. setalocador (TRANSip. h)
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
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748185"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>Método CTransInPlaceOutputPin. setalocador

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

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O pino de saída para esse filtro nunca fornece um alocador. Esse método especifica o alocador para o pino de saída. Ele define o valor da variável de membro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




