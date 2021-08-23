---
description: O método InitAllocator cria um alocador de memória.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Inimétodo tAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce1e8f8097ca88d0434f79c20e855d8b61798b5a1b0e32b6a38077e4c7aa1271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652456"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.Inimétodo tAllocator

O `InitAllocator` método cria um alocador de memória.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAlloc* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator do**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) alocador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um código de erro da **função CoCreateInstance.**

## <a name="remarks"></a>Comentários

Se o pin de entrada não fornecer um alocador de memória, o método [**CBaseOutputPin::D eputaçãoAllocator**](cbaseoutputpin-decideallocator.md) chamará esse método para criar um alocador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




