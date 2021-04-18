---
description: O método BreakConnect libera o PIN de uma conexão.
ms.assetid: 73b228a9-0a59-4647-b400-c33fa06c7e34
title: Método CBaseInputPin. BreakConnect (Amfilter. h)
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
ms.openlocfilehash: 6981ef97b98cc25b1996f1599d6d66b8e7d41f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750679"
---
# <a name="cbaseinputpinbreakconnect-method"></a>Método CBaseInputPin. BreakConnect

O `BreakConnect` método libera o PIN de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Ele desconfirma o alocador e libera a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Se você substituir esse método, chame o método de classe base do seu método de substituição. Caso contrário, você pode causar vazamentos de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




