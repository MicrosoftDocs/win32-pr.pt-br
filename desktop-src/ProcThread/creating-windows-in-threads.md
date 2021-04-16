---
description: Qualquer thread pode criar uma janela.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Criando janelas em threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787040"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="56717-103">Criando janelas em threads</span><span class="sxs-lookup"><span data-stu-id="56717-103">Creating Windows in Threads</span></span>

<span data-ttu-id="56717-104">Qualquer thread pode criar uma janela.</span><span class="sxs-lookup"><span data-stu-id="56717-104">Any thread can create a window.</span></span> <span data-ttu-id="56717-105">O thread que cria a janela possui a janela e sua fila de mensagens associada.</span><span class="sxs-lookup"><span data-stu-id="56717-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="56717-106">Portanto, o thread deve fornecer um loop de mensagem para processar as mensagens em sua fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="56717-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="56717-107">Além disso, você deve usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) nesse thread, em vez de outras [funções Wait](/windows/desktop/Sync/wait-functions), para que ele possa processar mensagens.</span><span class="sxs-lookup"><span data-stu-id="56717-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="56717-108">Caso contrário, o sistema poderá ser bloqueado quando o thread receber uma mensagem enquanto estiver aguardando.</span><span class="sxs-lookup"><span data-stu-id="56717-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="56717-109">A função [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) pode ser usada para permitir que um conjunto de threads Compartilhe o mesmo estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="56717-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="56717-110">Ao compartilhar o estado de entrada, os threads compartilham seu conceito de janela ativa.</span><span class="sxs-lookup"><span data-stu-id="56717-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="56717-111">Ao fazer isso, um thread sempre pode ativar outra janela do thread.</span><span class="sxs-lookup"><span data-stu-id="56717-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="56717-112">Essa função também é útil para compartilhar o estado de foco, o estado de captura do mouse, o estado do teclado e o estado de ordem Z da janela entre o Windows criado por diferentes threads cujo estado de entrada é compartilhado.</span><span class="sxs-lookup"><span data-stu-id="56717-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="56717-113">Para obter informações sobre como criar janelas, consulte [classes do Windows](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="56717-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
