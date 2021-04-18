---
description: O método PreparePerformanceData define os \_ valores m trLate e m \_ trFrame do quadro atual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
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
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749026"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Método CBaseVideoRenderer. PreparePerformanceData

O `PreparePerformanceData` método define os valores **m \_ trLate** e **m \_ trFrame** do quadro atual.

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

Valor que indica o quão tarde o exemplo estava além do tempo de vida, em unidades de tempo de referência.

</dd> <dt>

*trFrame* 
</dt> <dd>

Tempo entre quadros, em unidades de tempo de referência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro **define m \_ trLate** como o valor de *trLate* e **m \_ trFrame** como o valor de *trFrame*.

Quando a função de membro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) é chamada de [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) ou [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), ela passa os valores de **m \_ trLate** e **m \_ trFrame** para que ele atualize as estatísticas. `PreparePerformanceData` é chamado de [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) para definir esses valores de membro de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




