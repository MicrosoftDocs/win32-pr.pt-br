---
description: 'O método getpositiones recupera a posição atual e a posição de parada, em relação à duração total do fluxo. Esse método implementa o método IMediaSeeking:: getposicionations.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Método CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748019"
---
# <a name="cpospassthrugetpositions-method"></a>Método CPosPassThru. getpositiones

O `GetPositions` método recupera a posição atual e a posição de parada, em relação à duração total do fluxo. Esse método implementa o método [**IMediaSeeking:: Getposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .

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

Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição de parada, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




