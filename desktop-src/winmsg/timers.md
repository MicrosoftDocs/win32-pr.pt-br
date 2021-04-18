---
description: Este tópico discute os temporizadores. Um temporizador é uma rotina interna que mede repetidamente um intervalo especificado, em milissegundos.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810897"
---
# <a name="timers"></a><span data-ttu-id="501df-104">Temporizadores</span><span class="sxs-lookup"><span data-stu-id="501df-104">Timers</span></span>

<span data-ttu-id="501df-105">Um temporizador é uma rotina interna que mede repetidamente um intervalo especificado, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="501df-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="501df-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="501df-106">In This Section</span></span>



| <span data-ttu-id="501df-107">Nome</span><span class="sxs-lookup"><span data-stu-id="501df-107">Name</span></span>                                   | <span data-ttu-id="501df-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="501df-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="501df-109">Sobre temporizadores</span><span class="sxs-lookup"><span data-stu-id="501df-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="501df-110">Descreve como criar, identificar, definir e excluir temporizadores.</span><span class="sxs-lookup"><span data-stu-id="501df-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="501df-111">Usando temporizadores</span><span class="sxs-lookup"><span data-stu-id="501df-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="501df-112">Discute como criar e destruir temporizadores e como usar um temporizador para interceptar a entrada do mouse em intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="501df-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="501df-113">Referência do temporizador</span><span class="sxs-lookup"><span data-stu-id="501df-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="501df-114">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="501df-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="501df-115">Funções de temporizador</span><span class="sxs-lookup"><span data-stu-id="501df-115">Timer Functions</span></span>



| <span data-ttu-id="501df-116">Nome</span><span class="sxs-lookup"><span data-stu-id="501df-116">Name</span></span>                           | <span data-ttu-id="501df-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="501df-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="501df-118">**KillTimer**</span><span class="sxs-lookup"><span data-stu-id="501df-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="501df-119">Destrói o temporizador especificado.</span><span class="sxs-lookup"><span data-stu-id="501df-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="501df-120">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="501df-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="501df-121">Cria um temporizador com o valor de tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="501df-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="501df-122">*TimerProc*</span><span class="sxs-lookup"><span data-stu-id="501df-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="501df-123">Uma função de retorno de chamada definida pelo aplicativo que processa mensagens de [**\_ temporizador do WM**](wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="501df-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="501df-124">O tipo **TIMERPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="501df-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="501df-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) é um espaço reservado para o nome da função definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="501df-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="501df-126">Notificações de timer</span><span class="sxs-lookup"><span data-stu-id="501df-126">Timer Notifications</span></span>



| <span data-ttu-id="501df-127">Nome</span><span class="sxs-lookup"><span data-stu-id="501df-127">Name</span></span>                          | <span data-ttu-id="501df-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="501df-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="501df-129">**\_temporizador do WM**</span><span class="sxs-lookup"><span data-stu-id="501df-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="501df-130">Postado na fila de mensagens do thread de instalação quando um temporizador expira.</span><span class="sxs-lookup"><span data-stu-id="501df-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="501df-131">A mensagem é postada pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="501df-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
