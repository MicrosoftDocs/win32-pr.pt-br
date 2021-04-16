---
description: O método getrealstate recupera o estado do filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Método CBaseRenderer. getrealstate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752507"
---
# <a name="cbaserenderergetrealstate-method"></a>Método CBaseRenderer. getrealstate

O `GetRealState` método recupera o estado do filtro.

## <a name="syntax"></a>Sintaxe


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o valor do [**\_ estado CBaseFilter:: m**](cbasefilter-m-state.md). O valor é um membro do tipo enumerado de [**\_ estado do filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .

## <a name="remarks"></a>Comentários

Esse método fornece uma alternativa mais simples ao método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) , para uso interno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




