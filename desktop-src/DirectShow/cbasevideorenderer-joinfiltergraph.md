---
description: O método JoinFilterGraph envia a notificação de evento EC \_ WINDOW \_ DESTROYED quando um filtro é removido do grafo de filtro.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer.JoinFilterGraph (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052206"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Método CBaseVideoRenderer.JoinFilterGraph

O `JoinFilterGraph` método envia a [**notificação de evento EC WINDOW \_ \_ DESTROYED**](ec-window-destroyed.md) quando um filtro é removido do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Ponteiro para o grafo de filtro a ser junção.

</dd> <dt>

*pName* \[ Em\]
</dt> <dd>

Ponteiro para o nome do filtro que está sendo adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa função membro substitui a função de membro [**CBaseFilter::JoinFilterGraph.**](cbasefilter-joinfiltergraph.md) Se o filtro estiver deixando o grafo de filtro *(pGraph* é **NULL),** ele enviará uma notificação de evento [**EC WINDOW \_ \_ DESTROYED**](ec-window-destroyed.md) para que o gerenciador de recursos não mantenha o renderdor como um objeto de foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




