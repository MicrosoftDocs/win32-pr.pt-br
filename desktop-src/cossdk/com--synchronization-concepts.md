---
description: Geralmente, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartamento fornece a sincronização para você.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceitos de sincronização COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646494"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="ae154-103">Conceitos de sincronização COM+</span><span class="sxs-lookup"><span data-stu-id="ae154-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="ae154-104">Geralmente, a sincronização não é necessária quando você tem um STA (single-threaded apartment) porque o apartamento fornece a sincronização para você.</span><span class="sxs-lookup"><span data-stu-id="ae154-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="ae154-105">A sincronização se torna importante quando você tem um MTA (multithreaded apartment) e um objeto de thread livre.</span><span class="sxs-lookup"><span data-stu-id="ae154-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="ae154-106">No passado, os objetos de thread livre tinham que lidar com o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ae154-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="ae154-107">Você pode eliminar a necessidade de usar o bloqueio definindo o atributo de sincronização para um componente.</span><span class="sxs-lookup"><span data-stu-id="ae154-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="ae154-108">A sincronização tem as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="ae154-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="ae154-109">Permite que um chamador insira o componente por vez.</span><span class="sxs-lookup"><span data-stu-id="ae154-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="ae154-110">Proíbe o fluxo no processo ou no computador.</span><span class="sxs-lookup"><span data-stu-id="ae154-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="ae154-111">Flui de componente para componente dentro de um processo.</span><span class="sxs-lookup"><span data-stu-id="ae154-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="ae154-112">Permite a reentrância do mesmo chamador.</span><span class="sxs-lookup"><span data-stu-id="ae154-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="ae154-113">Ao contrário de Apartments, as atividades abrangem contextos de vários processos e hosts.</span><span class="sxs-lookup"><span data-stu-id="ae154-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="ae154-114">A sincronização determina qual atividade conterá um objeto.</span><span class="sxs-lookup"><span data-stu-id="ae154-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="ae154-115">Os objetos podem residir em qualquer uma das seguintes atividades:</span><span class="sxs-lookup"><span data-stu-id="ae154-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="ae154-116">Atividade do criador</span><span class="sxs-lookup"><span data-stu-id="ae154-116">Creator's activity</span></span>
-   <span data-ttu-id="ae154-117">Nova atividade</span><span class="sxs-lookup"><span data-stu-id="ae154-117">New activity</span></span>
-   <span data-ttu-id="ae154-118">Nenhuma atividade</span><span class="sxs-lookup"><span data-stu-id="ae154-118">No activity</span></span>

<span data-ttu-id="ae154-119">O COM+ garante a simultaneidade por uma série de bloqueios para cada atividade.</span><span class="sxs-lookup"><span data-stu-id="ae154-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="ae154-120">Se um chamador tentar inserir um componente sincronizado COM+ que já está sendo usado por outro chamador, a chamada será bloqueada até que o bloqueio seja liberado.</span><span class="sxs-lookup"><span data-stu-id="ae154-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="ae154-121">Esse comportamento de bloqueio não atingirá o tempo limite e não poderá ser configurado para atingir o tempo limite. Se o bloqueio não estiver em uso, o bloqueio será adquirido e a chamada será processada.</span><span class="sxs-lookup"><span data-stu-id="ae154-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="ae154-122">Após a conclusão, o bloqueio será liberado para o próximo chamador.</span><span class="sxs-lookup"><span data-stu-id="ae154-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="ae154-123">Para evitar o deadlock, o COM+ gerencia o acesso a todos os objetos entre as atividades por uma série aninhada de chamadas encadeadas em toda a rede.</span><span class="sxs-lookup"><span data-stu-id="ae154-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="ae154-124">O COM+ fornece as seguintes configurações de sincronização:</span><span class="sxs-lookup"><span data-stu-id="ae154-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="ae154-125">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="ae154-125">Disabled</span></span>
-   <span data-ttu-id="ae154-126">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="ae154-126">Not Supported</span></span>
-   <span data-ttu-id="ae154-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ae154-127">Supported</span></span>
-   <span data-ttu-id="ae154-128">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae154-128">Required</span></span>
-   <span data-ttu-id="ae154-129">Requer novo</span><span class="sxs-lookup"><span data-stu-id="ae154-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="ae154-130">Algumas configurações de sincronização funcionam em conjunto com outras configurações de componente COM+.</span><span class="sxs-lookup"><span data-stu-id="ae154-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="ae154-131">Por exemplo, a sincronização será necessária se o serviço de [ativação JIT (just-in-time) do com+](com--just-in-time-activation.md) estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="ae154-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="ae154-132">O JIT é necessário se você habilitar transações; Portanto, o [processamento de transações](com--transactions.md) com+ também requer sincronização.</span><span class="sxs-lookup"><span data-stu-id="ae154-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="ae154-133">Portanto, as classes com a configuração de JIT = true também devem ter a configuração de Synchronization = Required ou Synchronization = RequiresNew.</span><span class="sxs-lookup"><span data-stu-id="ae154-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="ae154-134">Para obter instruções sobre como definir as opções de sincronização usando a ferramenta administrativa serviços de componentes, consulte [definindo o atributo de sincronização](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="ae154-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="ae154-135">Para obter mais informações sobre como usar a biblioteca de administração do COM+ para definir opções de sincronização, consulte [automatizando a administração do com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="ae154-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae154-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae154-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae154-137">Tarefas de sincronização COM+</span><span class="sxs-lookup"><span data-stu-id="ae154-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



