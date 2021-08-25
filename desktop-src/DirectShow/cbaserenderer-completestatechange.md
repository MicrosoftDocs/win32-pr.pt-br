---
description: O método CompleteStateChange determina se uma transição para o estado em pausa foi concluída.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer.CompleteStateChange (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872356"
---
# <a name="cbaserenderercompletestatechange-method"></a>Método CBaseRenderer.CompleteStateChange

O `CompleteStateChange` método determina se uma transição para o estado pausado foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Oldstate* 
</dt> <dd>

Estado antes da transição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se a transição for concluída. Caso contrário, retornará S \_ FALSE.

## <a name="remarks"></a>Comentários

O [**método CBaseRenderer::P ause**](cbaserenderer-pause.md) chama esse método para atualizar o status de transição de estado. Em geral, a transição para pausada não termina até que o filtro receba um exemplo. No entanto, em algumas situações, a transição é concluída imediatamente: por exemplo, se o filtro estiver desconectado ou se o final do fluxo foi atingido. Esse método verifica os vários critérios e, em seguida, chama o método [**CBaseRenderer::Ready**](cbaserenderer-ready.md) ou o [**método CBaseRenderer::NotReady**](cbaserenderer-notready.md) para atualizar o status de transição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




