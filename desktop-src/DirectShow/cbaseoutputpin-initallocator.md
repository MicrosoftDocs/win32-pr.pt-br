---
description: O método InitAllocator cria um alocador de memória.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Inimétodo tAllocator (Amfilter. h)
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
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769245"
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

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um código de erro da função **CoCreateInstance** .

## <a name="remarks"></a>Comentários

Se o pino de entrada não fornecer um alocador de memória, o método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chamará esse método para criar um alocador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




