---
description: O método GetCurrentPosition recupera a posição atual, em relação à duração total do fluxo. Não implementado.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Método CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752080"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Método CSourceSeeking. GetCurrentPosition

O `GetCurrentPosition` método recupera a posição atual, em relação à duração total do fluxo. Não implementado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Os filtros de origem normalmente não dão suporte a esse método. Em vez disso, os filtros de renderização relatam a posição atual por meio da classe [**CRendererPosPassThru**](crendererpospassthru.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




