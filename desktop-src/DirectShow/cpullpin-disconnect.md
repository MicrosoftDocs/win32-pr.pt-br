---
description: O método Disconnect interrompe a conexão com o pino de saída.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Método CPullPin. Disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0491bfba7e5b739a2b46674cc2f6506017810d4f1e51693d4478720c67a4a4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055066"
---
# <a name="cpullpindisconnect-method"></a>Método CPullPin. Disconnect

O `Disconnect` método interrompe a conexão com o pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

esse método interrompe qualquer conexão feita no método [**CPullPin:: Conexão**](cpullpin-connect.md) . Chame esse método dentro de seu método [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) . (Se o PIN deriva de [**CBasePin**](cbasepin.md), substitua [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para chamar esse método.)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




