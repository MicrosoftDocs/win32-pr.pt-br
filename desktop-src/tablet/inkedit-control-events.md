---
description: 'A tabela a seguir descreve em quais threads os eventos de controle InkEdit podem ser acionados. EventThreadsChangeFires na interface do usuário do aplicativo (UI) threadClickFires na interface de usuários do aplicativo threadDblClickFires na interface do usuário do aplicativo threadGestureFires na interface do usuário do aplicativo threadKeyDownFires na interface do usuário do aplicativo threadKeyPressFires na interface do usuário do aplicativo threadKeyUpFires na interface do usuário do aplicativo threadMouseDownFires no threadMouseMoveFires da interface do usuário do aplicativo na threadMouseUpFires da interface do usuário do aplicativo (somente biblioteca gerenciada). Acionado na interface do usuário do aplicativo threadRecognitionResultFires na interface do usuário do aplicativo threadSelChangeFires na interface do usuário do aplicativo threadStrokeFires no thread da interface do usuário do aplicativo '
ms.assetid: 8554a1ab-3288-4bdd-866b-dd2c25842b1f
title: Eventos de controle InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b1547df05b438e6ade49663f5095dfd6674dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922485"
---
# <a name="inkedit-control-events"></a><span data-ttu-id="cca5b-103">Eventos de controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="cca5b-103">InkEdit Control Events</span></span>

<span data-ttu-id="cca5b-104">A tabela a seguir descreve em quais threads os eventos de controle [InkEdit](inkedit-control-reference.md) podem ser acionados.</span><span class="sxs-lookup"><span data-stu-id="cca5b-104">The following table describes which threads the [InkEdit](inkedit-control-reference.md) control events can fire on.</span></span>



| <span data-ttu-id="cca5b-105">Evento</span><span class="sxs-lookup"><span data-stu-id="cca5b-105">Event</span></span>                                                                          | <span data-ttu-id="cca5b-106">Threads</span><span class="sxs-lookup"><span data-stu-id="cca5b-106">Threads</span></span>                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="cca5b-107">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="cca5b-107">**Change**</span></span>](inkedit-change.md)                                               | <span data-ttu-id="cca5b-108">Acionado no thread da interface do usuário (IU) do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-108">Fires on the application's user interface (UI) thread</span></span><br/> |
| [<span data-ttu-id="cca5b-109">**Clicar**</span><span class="sxs-lookup"><span data-stu-id="cca5b-109">**Click**</span></span>](inkedit-click.md)                                                 | <span data-ttu-id="cca5b-110">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-110">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-111">**DblClick**</span><span class="sxs-lookup"><span data-stu-id="cca5b-111">**DblClick**</span></span>](inkedit-dblclick.md)                                           | <span data-ttu-id="cca5b-112">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-112">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-113">**Gesto**</span><span class="sxs-lookup"><span data-stu-id="cca5b-113">**Gesture**</span></span>](inkedit-gesture.md)                                             | <span data-ttu-id="cca5b-114">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-114">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-115">**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="cca5b-115">**KeyDown**</span></span>](inkedit-keydown.md)                                             | <span data-ttu-id="cca5b-116">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-116">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-117">**Pressionar**</span><span class="sxs-lookup"><span data-stu-id="cca5b-117">**KeyPress**</span></span>](inkedit-keypress.md)                                           | <span data-ttu-id="cca5b-118">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-118">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-119">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="cca5b-119">**KeyUp**</span></span>](inkedit-keyup.md)                                                 | <span data-ttu-id="cca5b-120">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-120">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-121">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="cca5b-121">**MouseDown**</span></span>](inkedit-mousedown.md)                                         | <span data-ttu-id="cca5b-122">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-122">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-123">**Ocorra**</span><span class="sxs-lookup"><span data-stu-id="cca5b-123">**MouseMove**</span></span>](inkedit-mousemove.md)                                         | <span data-ttu-id="cca5b-124">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-124">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-125">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="cca5b-125">**MouseUp**</span></span>](inkedit-mouseup.md)                                             | <span data-ttu-id="cca5b-126">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-126">Fires on the application's UI thread</span></span><br/>                  |
| <span data-ttu-id="cca5b-127">[**Reconhecimento**](/previous-versions/ms567627(v=vs.100)) (somente biblioteca gerenciada).</span><span class="sxs-lookup"><span data-stu-id="cca5b-127">[**Recognition**](/previous-versions/ms567627(v=vs.100)) (Managed Library only).</span></span> | <span data-ttu-id="cca5b-128">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-128">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-129">**RecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="cca5b-129">**RecognitionResult**</span></span>](inkedit-recognitionresult.md)                         | <span data-ttu-id="cca5b-130">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-130">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-131">**SelChange**</span><span class="sxs-lookup"><span data-stu-id="cca5b-131">**SelChange**</span></span>](inkedit-selchange.md)                                         | <span data-ttu-id="cca5b-132">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-132">Fires on the application's UI thread</span></span><br/>                  |
| [<span data-ttu-id="cca5b-133">**Pincel**</span><span class="sxs-lookup"><span data-stu-id="cca5b-133">**Stroke**</span></span>](inkedit-stroke.md)                                               | <span data-ttu-id="cca5b-134">Acionado no thread da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cca5b-134">Fires on the application's UI thread</span></span><br/>                  |



 

 

