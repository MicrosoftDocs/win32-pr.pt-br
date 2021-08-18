---
title: Evento TransportParametersUpdate
description: Ocorre sempre que qualquer um dos parâmetros de transporte é atualizado na DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate event Media Streaming API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034514"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Ocorre sempre que qualquer um dos parâmetros de transporte é atualizado na DMR.

## <a name="syntax"></a>Sintaxe


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para manipular notificações desse evento, registre uma função de manipulador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando o [**método add \_ TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) Para remover o registro do manipulador de eventos, use o [**\_ método remove TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)

 

 