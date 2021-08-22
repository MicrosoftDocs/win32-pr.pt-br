---
description: O método Render renderiza um exemplo.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Método CBaseRenderer. Render (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 185baf6818d2022dbe7b64cfab888945e1a2405433eefa925d2de70dcca286e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016854"
---
# <a name="cbaserendererrender-method"></a>Método CBaseRenderer. render

O `Render` método renderiza um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                             | Descrição                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O filtro está parado ou *pMediaSample* é **nulo**.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                              |



 

## <a name="remarks"></a>Comentários

Esse método chama o método virtual puro [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), que faz o trabalho real. A classe derivada deve implementar **DoRenderSample**.

Imediatamente antes de chamar **DoRenderSample**, esse método chama o método [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) . Imediatamente depois, ele chama o método [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) . A classe derivada pode substituir esses dois métodos conforme necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




