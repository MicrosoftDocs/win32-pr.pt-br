---
description: O método SendRepaint envia um evento Repaint para o Gerenciador do grafo de filtro.
ms.assetid: 78e5c46c-ca5d-4c5d-9dfc-992ce6b150ad
title: Método CBaseRenderer. SendRepaint (Renbase. h)
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
# <a name="cbaserenderersendrepaint-method"></a>Método CBaseRenderer. SendRepaint

O `SendRepaint` método envia um evento Repaint para o Gerenciador do grafo de filtro.

## <a name="syntax"></a>Sintaxe


```C++
void SendRepaint();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método envia um evento de [**\_ redesenho de EC**](ec-repaint.md) para o Gerenciador do grafo de filtro se as seguintes condições forem verdadeiras:

-   O pino de entrada está conectado.
-   O filtro não está liberando dados.
-   O fim do fluxo não foi atingido.
-   O sinalizador [**\_ bAbort CBaseRenderer:: m**](cbaserenderer-m-babort.md) é **false**.
-   O sinalizador [**\_ bRepaintStatus CBaseRenderer:: m**](cbaserenderer-m-brepaintstatus.md) é **true**.

Dependendo do estado do grafo, o \_ evento REpaint do EC pode fazer com que o filtro upstream envie novamente um exemplo; o grafo de filtro para buscar seu local atual ou o Gerenciador de gráficos de filtro para pausar momentaneamente. (Confira [**EC \_ Repaint**](ec-repaint.md).) Esse evento é potencialmente ineficiente, portanto, deve ser usado com moderação. No entanto, os renderizadores de vídeo às vezes precisam atualizar a exibição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




