---
description: O método JoinFilterGraph envia a \_ \_ notificação de evento destruída da janela do EC quando um filtro é removido do gráfico de filtro.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
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
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757709"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Método CBaseVideoRenderer. JoinFilterGraph

O `JoinFilterGraph` método envia a notificação de evento da [**janela do EC \_ \_ destruída**](ec-window-destroyed.md) quando um filtro é removido do gráfico de filtro.

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

Ponteiro para o gráfico de filtro a ser associado.

</dd> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para o nome do filtro que está sendo adicionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa função de membro substitui a função de membro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) . Se o filtro estiver deixando o grafo de filtro (*pGraph* é **nulo**), ele enviará uma notificação de evento de [**janela do EC \_ \_ destruída**](ec-window-destroyed.md) para que o Gerenciador de recursos não mantenha o processador como um objeto de foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




