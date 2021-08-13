---
description: Método CBaseInputPin.BreakConnect – o método BreakConnect libera o pino de uma conexão.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin.BreakConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 625eab8cc070240d79456bff919317f884826fc6d14c26055b68de40aba4c969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403485"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Método CBaseInputPin.BreakConnect

O `BreakConnect` método libera o pino de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou **um valor HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método substitui o [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Ele descommite o alocador e libera a interface [**IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Se você substituir esse método, chame o método de classe base do método de substituição. Caso contrário, você poderá causar vazamentos de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




