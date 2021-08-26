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
ms.openlocfilehash: fa7e957fe97e06c6fb14fe3a9048048e351ac1baf4ff8f4dae25b3cf5863776e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043706"
---
# <a name="cdeferredcommandcancel-method"></a>Método CDeferredCommand. Cancel

O `Cancel` método cancela uma solicitação [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) enfileirada anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**. Retorna um **HRESULT** de [**CCmdQueue:: Remove**](ccmdqueue-remove.md) se a chamada gerar um erro. Retornará S \_ OK se for bem-sucedido.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




