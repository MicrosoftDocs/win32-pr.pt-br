---
description: As sessões de rastreamento de eventos registram eventos de um ou mais provedores.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controlando sessões de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967442"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="8ae86-103">Controlando sessões de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="8ae86-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="8ae86-104">As sessões de rastreamento de eventos registram eventos de um ou mais [provedores](providing-events.md).</span><span class="sxs-lookup"><span data-stu-id="8ae86-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="8ae86-105">O controlador define a sessão e habilita os provedores.</span><span class="sxs-lookup"><span data-stu-id="8ae86-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="8ae86-106">Definir a sessão normalmente inclui especificar o nome do arquivo de log e da sessão, o tipo de arquivo de log a ser usado e a resolução do carimbo de data/hora usado para registrar os eventos.</span><span class="sxs-lookup"><span data-stu-id="8ae86-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="8ae86-107">Os controladores também podem atualizar e consultar sessões de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="8ae86-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="8ae86-108">Os tópicos a seguir demonstram como definir e atualizar uma sessão e habilitar provedores de rastreamento de eventos:</span><span class="sxs-lookup"><span data-stu-id="8ae86-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="8ae86-109">Configurando e iniciando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="8ae86-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="8ae86-110">Configurando e iniciando uma sessão SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="8ae86-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="8ae86-111">Configurando e iniciando uma sessão do agente de log</span><span class="sxs-lookup"><span data-stu-id="8ae86-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="8ae86-112">Configurando e iniciando uma sessão de agente de log particular</span><span class="sxs-lookup"><span data-stu-id="8ae86-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="8ae86-113">Atualizando uma sessão de rastreamento de eventos</span><span class="sxs-lookup"><span data-stu-id="8ae86-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="8ae86-114">Recuperando dados de rastreamento de eventos adicionais</span><span class="sxs-lookup"><span data-stu-id="8ae86-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="8ae86-115">Para obter informações sobre como liberar e consultar sessões, consulte [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8ae86-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="8ae86-116">Somente os usuários que executam com privilégios administrativos elevados, os usuários no grupo de usuários de log de desempenho e os aplicativos executados como LocalSystem, LocalService ou NetworkService podem controlar sessões de rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="8ae86-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="8ae86-117">Para conceder a um usuário restrito a capacidade de controlar as sessões de rastreamento, adicione-as ao grupo de usuários de log de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8ae86-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="8ae86-118">**Windows XP e windows 2000:** Qualquer pessoa pode controlar uma sessão de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="8ae86-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 
