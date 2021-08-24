---
description: Método CBaseOutputPin. BreakConnect – o método BreakConnect libera o PIN de uma conexão.
ms.assetid: 0dec3c9d-1adf-4fa3-ab5a-c351053f8054
title: Método CBaseOutputPin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae03edb843a2b9c6f1cbc98a46c2464de0e76e2eecf5d77bc309efa2dd60fd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793215"
---
# <a name="cbaseoutputpinbreakconnect-method"></a>Método CBaseOutputPin. BreakConnect

O `BreakConnect` método libera o PIN de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Ele desconfirma o alocador e libera as interfaces [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) e [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

Se você substituir esse método, chame o método de classe base do seu método de substituição. Caso contrário, você pode causar vazamentos de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




