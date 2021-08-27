---
description: O método DoRenderSample renderiza um exemplo.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Método CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef91e7ad27d008f5dfdb83e5642ecba8ec68bc424824dca9c8aa068ec055f24f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076426"
---
# <a name="cbaserendererdorendersample-method"></a>Método CBaseRenderer. DoRenderSample

O `DoRenderSample` método renderiza um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. O comportamento depende totalmente do tipo de filtro que está sendo implementado. Um processador de vídeo, por exemplo, desenharia a imagem de vídeo contida no exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




