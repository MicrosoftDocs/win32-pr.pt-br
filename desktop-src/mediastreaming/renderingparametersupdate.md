---
title: Evento RenderingParametersUpdate
description: Ocorre sempre que qualquer um de um conjunto de parâmetros de controle de renderização é atualizado no DMR.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API de streaming de mídia de evento RenderingParametersUpdate
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293964"
---
# <a name="renderingparametersupdate-event"></a>Evento RenderingParametersUpdate

Ocorre sempre que qualquer um de um conjunto de parâmetros de controle de renderização é atualizado no DMR.

## <a name="syntax"></a>Sintaxe


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) usando o método [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) . Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .

 

 