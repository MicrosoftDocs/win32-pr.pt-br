---
description: O método WaitForRenderTime aguarda o tempo de apresentação do exemplo atual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer.WaitForRenderTime (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e590a09c2c6d4cc34728f5ec29db0d8f650d3a1e9cb663e5993acd2cebe4793f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157350"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Método CBaseRenderer.WaitForRenderTime

O `WaitForRenderTime` método aguarda o tempo de apresentação do exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT.**



| Código de retorno                                                                                           | Descrição                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                       |
| <dl> <dt>**ESTADO DO VFW \_ E \_ \_ ALTERADO**</dt> </dl> | O estado do filtro foi alterado antes da hora da apresentação chegar.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método aguarda até que um dos seguintes ocorra:

-   O tempo de apresentação do exemplo chega, momento em que o exemplo pode ser renderizado.
-   O filtro para ou começa a liberar dados.

Se o tempo de apresentação chegar, o [**evento \_ RenderEvent CBaseRenderer::m**](cbaserenderer-m-renderevent.md) será sinalizado. Se o estado mudar, [**o evento \_ ThreadSignal CBaseRenderer::m**](cbaserenderer-m-threadsignal.md) será sinalizado. Esse método aguarda ambos os eventos. A classe derivada pode substituir esse método para aguardar eventos adicionais, se necessário.

Esse método chama o [**método CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) quando a espera começa e o método [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) quando a espera é feita. Nenhum método faz nada na classe base, mas a classe derivada pode substituí-las.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




