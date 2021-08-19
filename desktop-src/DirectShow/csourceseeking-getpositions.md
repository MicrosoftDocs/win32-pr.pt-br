---
description: O método GetPositions recupera a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking::GetPositions.
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking.GetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b6f52d8d8b30a28d942d4395a465b9c7c49d0a23020ad212c81eb170d20ca0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073330"
---
# <a name="csourceseekinggetpositions-method"></a>Método CSourceSeeking.GetPositions

O `GetPositions` método recupera a posição atual e a posição de parada. Esse método implementa o [**método IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição inicial.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição de parada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Para o parâmetro *pCurrent,* esse método retorna o valor da variável de membro [**CSourceSeeking::m \_ rtStart,**](csourceseeking-m-rtstart.md) que representa a hora de busca mais recente, não a posição de streaming atual. No entanto, quando um aplicativo chama **IMediaSeeking::GetPositions** por meio do gerenciador de grafo de filtro, os valores normalmente vêm de um filtro do renderador, não de um filtro de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




