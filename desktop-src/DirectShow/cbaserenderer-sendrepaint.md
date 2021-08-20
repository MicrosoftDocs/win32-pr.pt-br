---
description: O método SendRepaint envia um evento de repaint para o gerenciador de grafo de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer.SendRepaint (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendRepaint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9057d1ff733c30da3b3b0d7e960607eadd033dcee0b26994478c6da9156a183e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954785"
---
# <a name="cbaserenderersendrepaint-method"></a>Método CBaseRenderer.SendRepaint

O `SendRepaint` método envia um evento de reint para o gerenciador de grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método envia um [**evento \_ EC REPAINT**](ec-repaint.md) para o gerenciador de grafo de filtro se as seguintes condições são verdadeiras:

-   O pino de entrada está conectado.
-   O filtro não está liberando dados.
-   O final do fluxo não foi atingido.
-   O [**sinalizador CBaseRenderer::m \_ bAbort**](cbaserenderer-m-babort.md) é **FALSE.**
-   O [**sinalizador CBaseRenderer::m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md) é **TRUE.**

Dependendo do estado do grafo, o evento EC REPAINT pode fazer com que o filtro upstream envie uma amostra de novo; o grafo de filtro para buscar o local atual ou o gerenciador de grafo de filtro para pausar \_ momentaneamente. (Consulte [**EC \_ REPAINT**](ec-repaint.md).) Esse evento é potencialmente ineficiente, portanto, ele deve ser usado com moderação. No entanto, os renderadores de vídeo às vezes precisam atualizar a exibição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




