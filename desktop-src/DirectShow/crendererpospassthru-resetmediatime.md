---
description: O método ResetMediaTime redefine os carimbos de data/hora armazenados em cache como zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru.ResetMediaTime (Ctlutil.h)
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
ms.openlocfilehash: f1babc39ad3329ec18be663ffcc6eb882933bead0be5f631ef82ce363391f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953806"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Método CRendererPosPassThru.ResetMediaTime

O `ResetMediaTime` método redefine os carimbos de data/hora armazenados em cache como zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O filtro deve chamar esse método sempre que os carimbos de data/hora armazenados em cache pelo [**método CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) se tornarem inválidos. Especificamente, ele deve chamar esse método em resposta aos métodos [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) [**e IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

Depois que esse método é chamado, o [**método CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) retorna zero para as horas de início e término.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




