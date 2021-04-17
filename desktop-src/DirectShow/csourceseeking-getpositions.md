---
description: 'O método getpositiones recupera a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: getposicionations.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Método CSourceSeeking. GetPositions (Ctlutil. h)
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
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748016"
---
# <a name="csourceseekinggetpositions-method"></a>Método CSourceSeeking. getpositiones

O `GetPositions` método recupera a posição atual e a posição de parada. Esse método implementa o método [**IMediaSeeking:: Getposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

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

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Para o parâmetro *pCurrent* , esse método retorna o valor da variável de membro [**CSourceSeeking:: m \_ rtStart**](csourceseeking-m-rtstart.md) , que representa a hora de busca mais recente, não a posição de streaming atual. No entanto, quando um aplicativo chama **IMediaSeeking:: getposições** por meio do Gerenciador de gráfico de filtro, os valores normalmente são provenientes de um filtro de processador, não de um filtro de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




