---
title: Design de filosofia de filas de comando e listas de comandos
description: As metas de habilitar a reutilização do trabalho de renderização e do dimensionamento multithread, exigiam alterações fundamentais em como os aplicativos do Direct3D enviam o trabalho de renderização para a GPU.
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- lista de comandos
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812275a630464dbe9137d587a672803f4d0c72f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103445"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a><span data-ttu-id="bbcf5-105">Design de filosofia de filas de comando e listas de comandos</span><span class="sxs-lookup"><span data-stu-id="bbcf5-105">Design Philosophy of Command Queues and Command Lists</span></span>

<span data-ttu-id="bbcf5-106">As metas de habilitar a reutilização do trabalho de renderização e do dimensionamento multithread, exigiam alterações fundamentais em como os aplicativos do Direct3D enviam o trabalho de renderização para a GPU.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-106">The goals of enabling reuse of rendering work and of multi-threaded scaling, required fundamental changes to how Direct3D apps submit rendering work to the GPU.</span></span> <span data-ttu-id="bbcf5-107">No Direct3D 12, o processo de envio do trabalho de renderização difere de versões anteriores de três maneiras importantes:</span><span class="sxs-lookup"><span data-stu-id="bbcf5-107">In Direct3D 12, the process of submitting rendering work differs from earlier versions in three important ways:</span></span>

<dl> 1. <span data-ttu-id="bbcf5-108">Eliminação do contexto imediato.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-108">Elimination of the immediate context.</span></span> <span data-ttu-id="bbcf5-109">Isso habilita o multithreading.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-109">This enables multi-threading.</span></span>  
2. <span data-ttu-id="bbcf5-110">Os aplicativos agora têm como as chamadas de renderização são agrupadas em itens de trabalho da GPU (unidade de processamento gráfico).</span><span class="sxs-lookup"><span data-stu-id="bbcf5-110">Apps now own how rendering calls are grouped into graphics processing unit (GPU) work items.</span></span> <span data-ttu-id="bbcf5-111">Isso permite reutilização.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-111">This enables re-use.</span></span>  
3. <span data-ttu-id="bbcf5-112">Os aplicativos agora controlam explicitamente quando o trabalho é enviado para a GPU.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-112">Apps now explicitly control when work is submitted to the GPU .</span></span> <span data-ttu-id="bbcf5-113">Isso habilita os itens 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-113">This enables items 1 and 2.</span></span>  
</dl>

-   [<span data-ttu-id="bbcf5-114">Remoção do contexto imediato</span><span class="sxs-lookup"><span data-stu-id="bbcf5-114">Removal of the immediate context</span></span>](#removal-of-the-immediate-context)
-   [<span data-ttu-id="bbcf5-115">Agrupamento de itens de trabalho da GPU</span><span class="sxs-lookup"><span data-stu-id="bbcf5-115">Grouping of GPU work items</span></span>](#grouping-of-gpu-work-items)
-   [<span data-ttu-id="bbcf5-116">Envio de trabalho de GPU</span><span class="sxs-lookup"><span data-stu-id="bbcf5-116">GPU work submission</span></span>](#gpu-work-submission)
-   [<span data-ttu-id="bbcf5-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbcf5-117">Related topics</span></span>](#related-topics)

## <a name="removal-of-the-immediate-context"></a><span data-ttu-id="bbcf5-118">Remoção do contexto imediato</span><span class="sxs-lookup"><span data-stu-id="bbcf5-118">Removal of the immediate context</span></span>

<span data-ttu-id="bbcf5-119">A maior alteração do Microsoft Direct3D 11 para o Microsoft Direct3D 12 é que não há mais um contexto único e imediato associado a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-119">The largest change from Microsoft Direct3D 11 to Microsoft Direct3D 12 is that there is no longer a single, immediate context associated with a device.</span></span> <span data-ttu-id="bbcf5-120">Em vez disso, para renderizar, os aplicativos criam listas de comandos nas quais as APIs de renderização tradicionais podem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-120">Instead, to render, apps create command lists in which traditional rendering APIs can be called.</span></span> <span data-ttu-id="bbcf5-121">Uma lista de comandos é semelhante ao método Render de um aplicativo do Direct3D 11 que usava o contexto imediato, pois ele contém chamadas que desenham primitivos ou alteram o estado de renderização.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-121">A command list looks similar to the render method of a Direct3D 11 app that used the immediate context in that it contains calls that draw primitives or change the rendering state.</span></span> <span data-ttu-id="bbcf5-122">Como contextos imediatos, cada lista de comandos não está livre de threads; no entanto, várias listas de comandos podem ser registradas simultaneamente, o que aproveita os processadores modernos de vários núcleos.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-122">Like immediate contexts, each command list is not free-threaded; however, multiple command lists can be recorded concurrently, which takes advantage of modern, multi-core processors.</span></span>

<span data-ttu-id="bbcf5-123">As listas de comandos são normalmente executadas uma vez.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-123">Command lists are typically executed once.</span></span> <span data-ttu-id="bbcf5-124">No entanto, uma lista de comandos pode ser executada várias vezes se o aplicativo garante que as execuções anteriores sejam concluídas antes de enviar novas execuções.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-124">However, a command list can be executed multiple times if the application ensures that the previous executions are complete before submitting new executions.</span></span> <span data-ttu-id="bbcf5-125">Para obter mais informações sobre sincronização de lista de comandos, consulte [executando e sincronizando listas de comandos](executing-and-synchronizing-command-lists.md).</span><span class="sxs-lookup"><span data-stu-id="bbcf5-125">For more information about command list synchronization, see [Executing and synchronizing command lists](executing-and-synchronizing-command-lists.md).</span></span>

## <a name="grouping-of-gpu-work-items"></a><span data-ttu-id="bbcf5-126">Agrupamento de itens de trabalho da GPU</span><span class="sxs-lookup"><span data-stu-id="bbcf5-126">Grouping of GPU work items</span></span>

<span data-ttu-id="bbcf5-127">Além das listas de comandos, o Direct3D 12 aproveita a funcionalidade presente em todos os hardwares hoje, adicionando um segundo nível de listas de comandos, que são chamadas de *pacotes*.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-127">In addition to command lists, Direct3D 12 takes advantage of functionality present in all hardware today by adding a second level of command lists, which are called *bundles*.</span></span> <span data-ttu-id="bbcf5-128">Para ajudar a distinguir esses dois tipos, as listas de comandos de primeiro nível podem ser referidas como *listas de comandos diretos*.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-128">To help to distinguish these two types, the first-level command lists can be referred to as *direct command lists*.</span></span> <span data-ttu-id="bbcf5-129">A finalidade dos pacotes é permitir que os aplicativos agrupem um pequeno número de comandos de API para depois, repetidas execuções de dentro de listas de comandos diretas.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-129">The purpose of bundles is to allow apps to group a small number of API commands together for later, repeated execution from within direct command lists.</span></span> <span data-ttu-id="bbcf5-130">No momento da criação de um pacote, o driver executará o máximo de pré-processamento possível para tornar a execução mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-130">At the time of creating a bundle, the driver will perform as much pre-processing as possible to make later execution efficient.</span></span> <span data-ttu-id="bbcf5-131">Os grupos podem ser executados em várias listas de comandos e várias vezes na mesma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-131">Bundles can then be executed from within multiple command lists and multiple times within the same command list.</span></span>

<span data-ttu-id="bbcf5-132">A reutilização de pacotes é um grande driver de eficiência aprimorada com threads de CPU única.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-132">The re-use of bundles is a large driver of improved efficiency with single CPU threads.</span></span> <span data-ttu-id="bbcf5-133">Como os pacotes são pré-processados e podem ser enviados várias vezes, há certas restrições em quais operações podem ser executadas em um pacote.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-133">Because bundles are pre-processed and can be submitted multiple times, there are certain restrictions on what operations can be performed within a bundle.</span></span> <span data-ttu-id="bbcf5-134">Para obter mais informações, consulte [criando e gravando listas de comandos e pacotes](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="bbcf5-134">For more information, see [Creating and recording command lists and bundles](recording-command-lists-and-bundles.md).</span></span>

## <a name="gpu-work-submission"></a><span data-ttu-id="bbcf5-135">Envio de trabalho de GPU</span><span class="sxs-lookup"><span data-stu-id="bbcf5-135">GPU work submission</span></span>

<span data-ttu-id="bbcf5-136">Para executar o trabalho na GPU, um aplicativo deve enviar explicitamente uma lista de comandos para uma fila de comandos associada ao dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-136">To execute work on the GPU, an app must explicitly submit a command list to a command queue associated with the Direct3D device.</span></span> <span data-ttu-id="bbcf5-137">Uma lista de comandos diretas pode ser enviada para execução várias vezes, mas o aplicativo é responsável por garantir que a lista de comandos diretas concluiu a execução na GPU antes de enviá-la novamente.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-137">A direct command list can be submitted for execution multiple times, but the app is responsible for ensuring that the direct command list has finished executing on the GPU before submitting it again.</span></span> <span data-ttu-id="bbcf5-138">Os grupos não têm restrições de uso simultâneos e podem ser executados várias vezes em várias listas de comandos, mas os pacotes não podem ser enviados diretamente a uma fila de comandos para execução.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-138">Bundles have no concurrent-use restrictions and can be executed multiple times in multiple command lists, but bundles cannot be directly submitted to a command queue for execution.</span></span>

<span data-ttu-id="bbcf5-139">Qualquer thread pode enviar uma lista de comandos a qualquer fila de comandos a qualquer momento e o tempo de execução serializará automaticamente o envio da lista de comandos na fila de comandos, preservando a ordem de envio.</span><span class="sxs-lookup"><span data-stu-id="bbcf5-139">Any thread may submit a command list to any command queue at any time, and the runtime will automatically serialize submission of the command list in the command queue while preserving the submission order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbcf5-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbcf5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbcf5-141">Envio de trabalho no Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bbcf5-141">Work Submission in Direct3D 12</span></span>](command-queues-and-command-lists.md)
</dt> </dl>

 

 




