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
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="c36f0-104">Evento RenderingParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="c36f0-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="c36f0-105">Ocorre sempre que qualquer um de um conjunto de parâmetros de controle de renderização é atualizado no DMR.</span><span class="sxs-lookup"><span data-stu-id="c36f0-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36f0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c36f0-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="c36f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c36f0-107">Parameters</span></span>

<span data-ttu-id="c36f0-108">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c36f0-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c36f0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c36f0-109">Return value</span></span>

<span data-ttu-id="c36f0-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c36f0-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c36f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c36f0-111">Remarks</span></span>

<span data-ttu-id="c36f0-112">Para lidar com notificações desse evento, registre uma função de manipulador de eventos [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) usando o método [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="c36f0-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="c36f0-113">Para cancelar o registro do manipulador de eventos, use o método [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="c36f0-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 