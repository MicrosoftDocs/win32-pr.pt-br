---
description: 'O método inativo notifica o PIN de que o filtro não está mais ativo. Esse método substitui o método CBasePin:: Inactive. Se o thread de streaming estiver ativo, esse método o interromperá e aguardará a saída do thread.'
ms.assetid: 82cf0f13-e563-4a0b-b2e1-25ab19f7ed78
title: Método CSourceStream. Inactive (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9d9424f4299d7a07ad98010846fa917307bd38eead028b4b8c38c40e2284c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687366"
---
# <a name="csourcestreaminactive-method"></a>Método CSourceStream. Inactive

O `Inactive` método notifica o PIN de que o filtro não está mais ativo. Esse método substitui o método [**CBasePin:: Inactive**](cbasepin-inactive.md) . Se o thread de streaming estiver ativo, esse método o interromperá e aguardará a saída do thread.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




