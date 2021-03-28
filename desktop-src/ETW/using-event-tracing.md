---
description: Os tópicos a seguir descrevem como usar a API do ETW para rastreamento de eventos.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Usando o rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164742"
---
# <a name="using-event-tracing"></a><span data-ttu-id="5e314-103">Usando o rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="5e314-103">Using Event Tracing</span></span>

<span data-ttu-id="5e314-104">Os tópicos a seguir descrevem como usar a API do ETW para rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="5e314-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="5e314-105">Tópico</span><span class="sxs-lookup"><span data-stu-id="5e314-105">Topic</span></span>                                                                          | <span data-ttu-id="5e314-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e314-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e314-107">Controlando sessões de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="5e314-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="5e314-108">Descreve como gerenciar sessões de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="5e314-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="5e314-109">Fornecendo eventos</span><span class="sxs-lookup"><span data-stu-id="5e314-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="5e314-110">Descreve como registrar e instrumentar um provedor de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="5e314-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="5e314-111">Consumindo eventos</span><span class="sxs-lookup"><span data-stu-id="5e314-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="5e314-112">Descreve como implementar funções de retorno de chamada usadas para consumir e processar eventos de um arquivo de log de rastreamento ou em tempo real.</span><span class="sxs-lookup"><span data-stu-id="5e314-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="5e314-113">Pré-processador de rastreamento de software do Windows</span><span class="sxs-lookup"><span data-stu-id="5e314-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="5e314-114">Fornece um mecanismo eficiente para registrar e consumir eventos que ocorrem durante a execução de um aplicativo ou driver.</span><span class="sxs-lookup"><span data-stu-id="5e314-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="5e314-115">Inclua o arquivo de cabeçalho Wmistr. h antes de incluir o arquivo de cabeçalho Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="5e314-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



