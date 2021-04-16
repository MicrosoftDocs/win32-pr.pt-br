---
description: Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Log de eventos (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9871fdb7c7b81bdf57a8c5de87a0a09d5a0570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105779222"
---
# <a name="event-logging-event-logging"></a><span data-ttu-id="9f5ca-103">Log de eventos (log de eventos)</span><span class="sxs-lookup"><span data-stu-id="9f5ca-103">Event Logging (Event Logging)</span></span>

<span data-ttu-id="9f5ca-104">Muitos aplicativos registram erros e eventos em logs de erros proprietários, cada um com seu próprio formato e interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-104">Many applications record errors and events in proprietary error logs, each with their own format and user interface.</span></span> <span data-ttu-id="9f5ca-105">Dados de diferentes aplicativos não podem ser mesclados facilmente em um relatório completo, exigindo que os administradores do sistema ou representantes de suporte verifiquem uma variedade de fontes para diagnosticar problemas.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-105">Data from different applications can't easily be merged into one complete report, requiring system administrators or support representatives to check a variety of sources to diagnose problems.</span></span>

<span data-ttu-id="9f5ca-106">O log de eventos fornece uma maneira padrão e centralizada para aplicativos (e o sistema operacional) para registrar eventos importantes de software e hardware.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-106">Event logging provides a standard, centralized way for applications (and the operating system) to record important software and hardware events.</span></span> <span data-ttu-id="9f5ca-107">O serviço de log de eventos registra eventos de várias fontes e os armazena em uma única coleção chamada *log de eventos*.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-107">The event logging service records events from various sources and stores them in a single collection called an *event log*.</span></span> <span data-ttu-id="9f5ca-108">O Visualizador de Eventos permite que você exiba logs; a interface de programação também permite que você examine os logs.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-108">The Event Viewer enables you to view logs; the programming interface also enables you to examine logs.</span></span>

-   [<span data-ttu-id="9f5ca-109">Sobre o log de eventos</span><span class="sxs-lookup"><span data-stu-id="9f5ca-109">About Event Logging</span></span>](about-event-logging.md)
-   [<span data-ttu-id="9f5ca-110">Usando o log de eventos</span><span class="sxs-lookup"><span data-stu-id="9f5ca-110">Using Event Logging</span></span>](using-event-logging.md)
-   [<span data-ttu-id="9f5ca-111">Referência de log de eventos</span><span class="sxs-lookup"><span data-stu-id="9f5ca-111">Event Logging Reference</span></span>](event-logging-reference.md)

> [!Note]  
> <span data-ttu-id="9f5ca-112">A API de log de eventos foi projetada para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-112">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="9f5ca-113">No Windows Vista, a infraestrutura de log de eventos foi reprojetada.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-113">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="9f5ca-114">Os aplicativos projetados para execução no Windows Vista ou em sistemas operacionais posteriores devem usar o [log de eventos do Windows](/windows/desktop/WES/windows-event-log) para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="9f5ca-114">Applications that are designed to run on Windows Vista or later operating systems should use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>
