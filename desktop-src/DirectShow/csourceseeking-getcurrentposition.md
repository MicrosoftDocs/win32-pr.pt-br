---
description: O método GetCurrentPosition recupera a posição atual, em relação à duração total do fluxo. Não implementado.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Método CSourceSeeking.GetCurrentPosition (Ctlutil.h)
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
ms.openlocfilehash: ff4069c8b1a83ade6897fedf87c16b89b1c63d3c1cef18d21a3bdbd594a3b2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084053"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Método CSourceSeeking.GetCurrentPosition

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

## <a name="return-value"></a>Valor retornado

Retorna E \_ NOTIMPL.

## <a name="remarks"></a>Comentários

Os filtros de origem normalmente não são suportados por esse método. Em vez disso, os filtros de renderização relatam a posição atual por meio da [**classe CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




