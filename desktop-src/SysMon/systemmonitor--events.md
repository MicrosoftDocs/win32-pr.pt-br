---
title: Eventos de SystemMonitor
description: A classe SystemMonitor tem os seguintes eventos
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756122"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="02133-103">Eventos de SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="02133-103">SystemMonitor Events</span></span>

<span data-ttu-id="02133-104">A classe [**SystemMonitor**](systemmonitor.md) tem os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="02133-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="02133-105">**OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="02133-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="02133-106">**OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="02133-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="02133-107">**OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="02133-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="02133-108">**AoClicarDuasVezes**</span><span class="sxs-lookup"><span data-stu-id="02133-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="02133-109">**OnSampleCollected**</span><span class="sxs-lookup"><span data-stu-id="02133-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="02133-110">Você deve retornar do manipulador de eventos antes que o [**intervalo de atualização**](systemmonitor-updateinterval.md) expire; caso contrário, o SYSMON exibirá uma caixa de mensagem indicando ao usuário que ele não pôde obter amostras de valores de contadores para o intervalo de atualização anterior.</span><span class="sxs-lookup"><span data-stu-id="02133-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




