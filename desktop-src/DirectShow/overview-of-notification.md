---
description: Visão geral da notificação de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Visão geral da notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645916"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="eba39-103">Visão geral da notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="eba39-103">Overview of Event Notification</span></span>

<span data-ttu-id="eba39-104">Um filtro notifica o Gerenciador de gráfico de filtro sobre um evento postando uma notificação de evento.</span><span class="sxs-lookup"><span data-stu-id="eba39-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="eba39-105">O evento pode ser algo esperado, como o fim de um fluxo, ou pode representar um erro, como uma falha para renderizar um fluxo.</span><span class="sxs-lookup"><span data-stu-id="eba39-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="eba39-106">O Gerenciador de gráficos de filtro trata alguns eventos de filtro por si só e deixa outros para que o aplicativo manipule.</span><span class="sxs-lookup"><span data-stu-id="eba39-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="eba39-107">Se o Gerenciador do grafo de filtro não manipular um evento de filtro, ele colocará a notificação de eventos em uma fila.</span><span class="sxs-lookup"><span data-stu-id="eba39-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="eba39-108">O grafo de filtro também pode enfileirar suas próprias notificações de eventos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eba39-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="eba39-109">Um aplicativo recupera eventos da fila e responde a eles com base no tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="eba39-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="eba39-110">A notificação de eventos no DirectShow é, portanto, semelhante ao esquema de enfileiramento de mensagens do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eba39-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="eba39-111">Um aplicativo também pode cancelar o comportamento padrão do Gerenciador de grafo de filtro para um determinado tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="eba39-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="eba39-112">O Gerenciador de gráfico de filtro coloca esses eventos diretamente na fila para que o aplicativo manipule.</span><span class="sxs-lookup"><span data-stu-id="eba39-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="eba39-113">Esse mecanismo habilita</span><span class="sxs-lookup"><span data-stu-id="eba39-113">This mechanism enables</span></span>

-   <span data-ttu-id="eba39-114">O Gerenciador do grafo de filtro para se comunicar com o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eba39-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="eba39-115">Filtros para se comunicar com o aplicativo e o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="eba39-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="eba39-116">O aplicativo para determinar seu grau de envolvimento na manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="eba39-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



