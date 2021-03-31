---
title: Registrando uma função de gancho
description: Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada WinEventProc. As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822449"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="96b80-104">Registrando uma função de gancho</span><span class="sxs-lookup"><span data-stu-id="96b80-104">Registering a Hook Function</span></span>

<span data-ttu-id="96b80-105">Os aplicativos cliente recebem WinEvents em uma função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) .</span><span class="sxs-lookup"><span data-stu-id="96b80-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="96b80-106">As ações executadas pela função de retorno de chamada são definidas pelo aplicativo, mas a sintaxe deve ser conforme especificado no protótipo.</span><span class="sxs-lookup"><span data-stu-id="96b80-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="96b80-107">Antes que possa receber eventos, a função deve ser registrada chamando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span><span class="sxs-lookup"><span data-stu-id="96b80-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="96b80-108">O cliente pode chamar **SetWinEventHook** mais de uma vez para registrar diferentes funções de gancho ou para definir eventos adicionais para uma função de gancho registrada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96b80-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="96b80-109">Ao chamar [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , o cliente especifica quais eventos receber e como recebê-los.</span><span class="sxs-lookup"><span data-stu-id="96b80-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="96b80-110">O cliente pode optar por:</span><span class="sxs-lookup"><span data-stu-id="96b80-110">The client can choose to:</span></span>

-   <span data-ttu-id="96b80-111">Receber todos os eventos ou um conjunto específico de eventos.</span><span class="sxs-lookup"><span data-stu-id="96b80-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="96b80-112">Receber eventos de todos os threads ou de um thread específico.</span><span class="sxs-lookup"><span data-stu-id="96b80-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="96b80-113">Receber eventos de todos os processos ou de um processo específico.</span><span class="sxs-lookup"><span data-stu-id="96b80-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="96b80-114">Manipule eventos em processo ou fora do processo.</span><span class="sxs-lookup"><span data-stu-id="96b80-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="96b80-115">Quando é gerado um evento que corresponde aos critérios especificados, o sistema chama a função de retorno de chamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) do cliente (ou "procedimento de gancho").</span><span class="sxs-lookup"><span data-stu-id="96b80-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="96b80-116">Os parâmetros que a função Hook recebe dizem ao cliente sobre a janela, o objeto e o elemento filho possível que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="96b80-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="96b80-117">Um cliente usa esses parâmetros em uma chamada de recuperação de objeto, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="96b80-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




