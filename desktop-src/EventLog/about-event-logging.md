---
description: Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar os dados perdidos e impedir que o erro seja recorrente.
ms.assetid: 2a625c8a-afa2-484a-a0e3-df3ef774abe4
title: Sobre o log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1104a4b54d2989cb329b665e20fd273766e57209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010603"
---
# <a name="about-event-logging"></a><span data-ttu-id="fb6b8-103">Sobre o log de eventos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-103">About Event Logging</span></span>

<span data-ttu-id="fb6b8-104">Quando ocorre um erro, o administrador do sistema ou o representante de suporte deve determinar o que causou o erro, tentar recuperar os dados perdidos e impedir que o erro seja recorrente.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-104">When an error occurs, the system administrator or support representative must determine what caused the error, attempt to recover any lost data, and prevent the error from recurring.</span></span> <span data-ttu-id="fb6b8-105">É útil se os aplicativos, o sistema operacional e outros serviços do sistema registram eventos importantes, como condições de pouca memória ou tentativas excessivas de acessar um disco.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-105">It is helpful if applications, the operating system, and other system services record important events, such as low-memory conditions or excessive attempts to access a disk.</span></span> <span data-ttu-id="fb6b8-106">O administrador do sistema pode, então, usar o log de eventos para ajudar a determinar quais condições provocaram o erro e identificar o contexto no qual ele ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-106">The system administrator can then use the event log to help determine what conditions caused the error and identify the context in which it occurred.</span></span> <span data-ttu-id="fb6b8-107">Ao Visualizar periodicamente o log de eventos, o administrador do sistema poderá identificar problemas (como um disco rígido com falha) antes que eles causem danos.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-107">By periodically viewing the event log, the system administrator may be able to identify problems (such as a failing hard disk) before they cause damage.</span></span>

> [!Note]  
> <span data-ttu-id="fb6b8-108">A API de log de eventos foi projetada para aplicativos executados no sistema operacional Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-108">The Event Logging API was designed for applications that run on the Windows Server 2003, Windows XP, or Windows 2000 operating system.</span></span> <span data-ttu-id="fb6b8-109">No Windows Vista, a infraestrutura de log de eventos foi reprojetada.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-109">In Windows Vista, the event logging infrastructure was redesigned.</span></span> <span data-ttu-id="fb6b8-110">Os aplicativos projetados para execução no Windows Vista ou em sistemas operacionais posteriores agora devem usar o [log de eventos do Windows](/windows/desktop/WES/windows-event-log) para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-110">Applications that are designed to run on the Windows Vista or later operating systems should now use [Windows Event Log](/windows/desktop/WES/windows-event-log) to log events.</span></span>

 
<span data-ttu-id="fb6b8-111">Esta seção aborda a interface de programação para escrever e consumir eventos usando o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-111">This section discusses the programming interface for writing and consuming events using Event Logging.</span></span>

-   [<span data-ttu-id="fb6b8-112">Tipos de evento</span><span class="sxs-lookup"><span data-stu-id="fb6b8-112">Event types</span></span>](event-types.md)
-   [<span data-ttu-id="fb6b8-113">Diretrizes de registro em log</span><span class="sxs-lookup"><span data-stu-id="fb6b8-113">Logging guidelines</span></span>](logging-guidelines.md)
-   [<span data-ttu-id="fb6b8-114">Elementos de log de eventos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-114">Event logging elements</span></span>](event-logging-elements.md)
-   [<span data-ttu-id="fb6b8-115">Operações de log de eventos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-115">Event logging operations</span></span>](event-logging-operations.md)
-   [<span data-ttu-id="fb6b8-116">Modelo de log de eventos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-116">Event logging model</span></span>](event-logging-model.md)
-   [<span data-ttu-id="fb6b8-117">Segurança do log de eventos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-117">Event logging security</span></span>](event-logging-security.md)

> [!Note]  
> <span data-ttu-id="fb6b8-118">Os aplicativos que publicam eventos maiores que 64 quilobytes em um computador com Windows Server 2003, Windows XP ou Windows 2000 não poderão publicar eventos em um computador Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-118">Applications that publish events that are larger than 64 kilobytes on a Windows Server 2003, Windows XP, or Windows 2000 computer will not be able to publish events on a Windows Vista or later computer.</span></span>
