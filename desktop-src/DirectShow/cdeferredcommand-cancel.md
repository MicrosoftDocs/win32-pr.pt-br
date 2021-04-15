---
description: 'O método Cancel cancela uma solicitação CDeferredCommand:: Invoke enfileirada anteriormente.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Método CDeferredCommand. Cancel (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747393"
---
# <a name="cdeferredcommandcancel-method"></a>Método CDeferredCommand. Cancel

O `Cancel` método cancela uma solicitação [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) enfileirada anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**. Retorna um **HRESULT** de [**CCmdQueue:: Remove**](ccmdqueue-remove.md) se a chamada gerar um erro. Retornará S \_ OK se for bem-sucedido.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




