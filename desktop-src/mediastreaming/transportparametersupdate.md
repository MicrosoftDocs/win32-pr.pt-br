---
title: Evento TransportParametersUpdate
description: Ocorre sempre que qualquer um de um conjunto de parâmetros de transporte é atualizado no DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API de streaming de mídia de evento TransportParametersUpdate
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823745"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Ocorre sempre que qualquer um de um conjunto de parâmetros de transporte é atualizado no DMR.

## <a name="syntax"></a>Sintaxe


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando o método [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 