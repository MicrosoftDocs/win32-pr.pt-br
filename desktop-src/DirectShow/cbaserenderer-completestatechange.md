---
description: O método CompleteStateChange determina se uma transição para o estado em pausa está concluída.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer. CompleteStateChange (Renbase. h)
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
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753347"
---
# <a name="cbaserenderercompletestatechange-method"></a>Método CBaseRenderer. CompleteStateChange

O `CompleteStateChange` método determina se uma transição para o estado em pausa está concluída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldState* 
</dt> <dd>

Estado anterior à transição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se a transição for concluída. Caso contrário, retornará S \_ false.

## <a name="remarks"></a>Comentários

O método [**CBaseRenderer::P ause**](cbaserenderer-pause.md) chama esse método para atualizar o status de transição de estado. Em geral, a transição para pausada não é concluída até que o filtro receba um exemplo. No entanto, em algumas situações a transição é concluída imediatamente: por exemplo, se o filtro estiver desconectado ou se o final do fluxo foi atingido. Esse método verifica os vários critérios e, em seguida, chama o método [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) ou o método [**CBaseRenderer:: não Ready**](cbaserenderer-notready.md) para atualizar o status da transição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




