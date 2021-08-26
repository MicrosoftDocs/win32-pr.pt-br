---
description: Método CBaseInputPin.GetAllocator – o método GetAllocator recupera o alocador de memória proposto por esse pino. Esse método implementa o método IMemInputPin::GetAllocator.
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin.GetAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 119f3ffaa5863584b55210306b38b011c758f9bab0febac47547bdfe469b5ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056336"
---
# <a name="cbaseinputpingetallocator-method"></a>Método CBaseInputPin.GetAllocator

O `GetAllocator` método recupera o alocador de memória proposto por esse pino. Esse método implementa o [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator do**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) alocador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um código de erro da **função CoCreateInstance.**

## <a name="remarks"></a>Comentários

Esse método cria um [**objeto CMemAllocator.**](cmemallocator.md) Substitua esse método se o filtro usar um alocador de um pin downstream ou um alocador personalizado.

Se o método for bem-sucedido, a interface **IMemAllocator** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




