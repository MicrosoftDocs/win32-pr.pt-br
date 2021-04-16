---
description: O método ResetMediaTime redefine os carimbos de data/hora em cache como zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752285"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Método CRendererPosPassThru. ResetMediaTime

O `ResetMediaTime` método redefine os carimbos de data/hora em cache como zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método sempre que os carimbos de data/hora armazenados em cache pelo método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) se tornarem inválidos. Especificamente, ele deve chamar esse método em resposta aos métodos [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) e [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

Depois que esse método é chamado, o método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) retorna zero para os horários de início e término.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




