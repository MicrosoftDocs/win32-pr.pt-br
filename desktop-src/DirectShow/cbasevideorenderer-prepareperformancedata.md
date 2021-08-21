---
description: O método PreparePerformanceData define os valores m \_ trLate e m \_ trFrame do quadro atual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer.PreparePerformanceData (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8cb276b37e64b6bb34751ed2d034666f7ceeddd90d8e52e47b2a1fca499ff9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658330"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Método CBaseVideoRenderer.PreparePerformanceData

O `PreparePerformanceData` método define os valores m **\_ trLate** e **m \_ trFrame** do quadro atual.

## <a name="syntax"></a>Sintaxe


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*trLate* 
</dt> <dd>

Valor que indica a atraso da amostra além do tempo devido, em unidades de tempo de referência.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tempo entre períodos, em unidades de tempo de referência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função membro define **m \_ trLate como** o valor de *trLate* e **m \_ trFrame** com o valor *de trFrame*.

Quando a função membro [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) é chamada de [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) ou [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), ela passa os valores **de m \_ trLate** e **m \_ trFrame** para que ele atualize as estatísticas. `PreparePerformanceData` é chamado de [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) para definir esses valores de membro de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




