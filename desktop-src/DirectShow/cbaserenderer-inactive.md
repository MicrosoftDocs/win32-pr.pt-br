---
description: O método inativo é chamado quando o estado é alternado para parado.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Método CBaseRenderer. Inactive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652396"
---
# <a name="cbaserendererinactive-method"></a>Método CBaseRenderer. Inactive

O `Inactive` método é chamado quando o estado é alternado para parado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O pino de entrada chama esse método de seu próprio método [**CRendererInputPin:: Inactive**](crendererinputpin-inactive.md) . O filtro chama o método [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) para liberar o exemplo mais recente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




