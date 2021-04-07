---
title: Log de eventos do Windows
description: A API do log de eventos do Windows define o esquema que você usa para gravar um manifesto de instrumentação.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823974"
---
# <a name="windows-event-log"></a><span data-ttu-id="aa1d4-103">Log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="aa1d4-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="aa1d4-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="aa1d4-104">Purpose</span></span>

<span data-ttu-id="aa1d4-105">A API do log de eventos do Windows define o esquema que você usa para gravar um manifesto de instrumentação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="aa1d4-106">Um manifesto de instrumentação identifica seu provedor de eventos e os eventos que ele registra.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="aa1d4-107">A API também inclui as funções que um consumidor de evento, como o [Visualizador de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), usaria para ler e renderizar os eventos.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="aa1d4-108">Para gravar os eventos definidos no manifesto, use as funções incluídas na API de [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="aa1d4-109">O log de eventos do Windows substitui a API de [log de eventos](/windows/desktop/EventLog/event-logging) que começa com o sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="aa1d4-110">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="aa1d4-110">Developer audience</span></span>

<span data-ttu-id="aa1d4-111">O log de eventos do Windows foi projetado para programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="aa1d4-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="aa1d4-112">Run-time requirements</span></span>

<span data-ttu-id="aa1d4-113">O log de eventos do Windows está incluído no sistema operacional a partir do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="aa1d4-114">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="aa1d4-115">Para obter o histórico completo de versões, consulte [novidades](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa1d4-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aa1d4-116">In this section</span></span>


| <span data-ttu-id="aa1d4-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="aa1d4-117">Topic</span></span>                                                        | <span data-ttu-id="aa1d4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa1d4-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa1d4-119">Usando o log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="aa1d4-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="aa1d4-120">Guia de procedimentos que mostra como usar a API do log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="aa1d4-121">Referência do log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="aa1d4-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="aa1d4-122">Os tipos de dados, as funções, as enumerações, as estruturas, as constantes e os esquemas que a API inclui.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|