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
# <a name="transportparametersupdate-event"></a><span data-ttu-id="91893-104">Evento TransportParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="91893-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="91893-105">Ocorre sempre que qualquer um de um conjunto de parâmetros de transporte é atualizado no DMR.</span><span class="sxs-lookup"><span data-stu-id="91893-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="91893-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91893-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="91893-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91893-107">Parameters</span></span>

<span data-ttu-id="91893-108">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="91893-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91893-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91893-109">Return value</span></span>

<span data-ttu-id="91893-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="91893-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91893-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="91893-111">Remarks</span></span>

<span data-ttu-id="91893-112">Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) usando o método [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="91893-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="91893-113">Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="91893-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 