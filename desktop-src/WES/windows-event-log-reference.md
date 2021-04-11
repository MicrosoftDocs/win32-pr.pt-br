---
title: Referência do log de eventos do Windows
description: A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de execução e consultar eventos de canais e arquivos de log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010125"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="7c1a8-103">Referência do log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-103">Windows Event Log Reference</span></span>

<span data-ttu-id="7c1a8-104">A seguir estão os elementos de programação que você usa para criar um manifesto de instrumentação, criar recursos do manifesto que seu provedor usa, obter metadados de instrumentação em tempo de execução e consultar eventos de canais e arquivos de log:</span><span class="sxs-lookup"><span data-stu-id="7c1a8-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="7c1a8-105">Esquema EventManifest</span><span class="sxs-lookup"><span data-stu-id="7c1a8-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="7c1a8-106">Esquema de evento</span><span class="sxs-lookup"><span data-stu-id="7c1a8-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="7c1a8-107">Esquema de consulta</span><span class="sxs-lookup"><span data-stu-id="7c1a8-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="7c1a8-108">Constantes do log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="7c1a8-109">Tipos de dados de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="7c1a8-110">Enumerações de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="7c1a8-111">Funções de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="7c1a8-112">Estruturas de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="7c1a8-113">Ferramentas de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="7c1a8-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="7c1a8-114">Para aplicativos escritos usando uma linguagem .NET, como C# ou Visual Basic, consulte os seguintes namespaces:</span><span class="sxs-lookup"><span data-stu-id="7c1a8-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="7c1a8-115">Para gravar eventos, use as classes e os métodos definidos no namespace [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="7c1a8-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="7c1a8-116">Para consumir eventos de um canal ou log de log de eventos do Windows, use as classes e os métodos definidos no namespace [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="7c1a8-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="7c1a8-117">Como alternativa ao uso do namespace [System. Diagnostics.](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) informativo para gravar eventos, você pode usar o argumento **-cs** ou **-CSS** para que o compilador de mensagens gere o código para gravar os eventos.</span><span class="sxs-lookup"><span data-stu-id="7c1a8-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="7c1a8-118">Para obter detalhes, consulte [**compilador de mensagem**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="7c1a8-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
