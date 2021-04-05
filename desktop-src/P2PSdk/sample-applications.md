---
title: Aplicativos de exemplo (infraestrutura de mesmo nível)
description: Os aplicativos de exemplo a seguir estão incluídos no Windows XP peer SDK.
ms.assetid: 26c45360-f232-4e29-90b5-44ccacb5a9c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c15e2bf3162151a4cbf18547fdfe482c7ea77fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921761"
---
# <a name="sample-applications-peer-infrastructure"></a><span data-ttu-id="45030-103">Aplicativos de exemplo (infraestrutura de mesmo nível)</span><span class="sxs-lookup"><span data-stu-id="45030-103">Sample applications (Peer Infrastructure)</span></span>

<span data-ttu-id="45030-104">Os aplicativos de exemplo a seguir estão incluídos no Windows XP peer SDK.</span><span class="sxs-lookup"><span data-stu-id="45030-104">The following sample applications are included in the Windows XP Peer SDK.</span></span> <span data-ttu-id="45030-105">Os exemplos podem ajudá-lo quando você desenvolver seus próprios aplicativos de mesmo nível usando a infraestrutura de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="45030-105">The samples can help you when you develop your own peer applications using the Peer Infrastructure.</span></span>

-   [<span data-ttu-id="45030-106">Chat do grafo</span><span class="sxs-lookup"><span data-stu-id="45030-106">Graph Chat</span></span>](#graph-chat)
-   [<span data-ttu-id="45030-107">Chat de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-107">Group Chat</span></span>](#group-chat)
-   [<span data-ttu-id="45030-108">Navegador de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-108">Group Browser</span></span>](#group-browser)

## <a name="graph-chat"></a><span data-ttu-id="45030-109">Chat do grafo</span><span class="sxs-lookup"><span data-stu-id="45030-109">Graph Chat</span></span>

<span data-ttu-id="45030-110">O aplicativo de exemplo de chat do grafo é um aplicativo de chat simples que demonstra como usar as APIs de grafo de pares e o provedor de Namespace PNRP (Peer Name Resolution Protocol) com a API do Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="45030-110">The Graph Chat sample application is a simple chat application that demonstrates how to use the Peer Graphing APIs and the Peer Name Resolution Protocol (PNRP) Namespace Provider with the Winsock 2 API.</span></span> <span data-ttu-id="45030-111">O aplicativo demonstra as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="45030-111">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="45030-112">Criando um grafo</span><span class="sxs-lookup"><span data-stu-id="45030-112">Creating a graph</span></span>
-   <span data-ttu-id="45030-113">Conectando a um grafo existente</span><span class="sxs-lookup"><span data-stu-id="45030-113">Connecting to an existing graph</span></span>
-   <span data-ttu-id="45030-114">Desconectando de um grafo existente</span><span class="sxs-lookup"><span data-stu-id="45030-114">Disconnecting from an existing graph</span></span>
-   <span data-ttu-id="45030-115">Enumerando entidades pares</span><span class="sxs-lookup"><span data-stu-id="45030-115">Enumerating peer entities</span></span>
-   <span data-ttu-id="45030-116">Adicionando registros ao grafo</span><span class="sxs-lookup"><span data-stu-id="45030-116">Adding records to the graph</span></span>
-   <span data-ttu-id="45030-117">Usando conexões diretas com um grafo</span><span class="sxs-lookup"><span data-stu-id="45030-117">Using direct connections with a graph</span></span>
-   <span data-ttu-id="45030-118">Usando a notificação e a infraestrutura de eventos com grafos</span><span class="sxs-lookup"><span data-stu-id="45030-118">Using the notification and event infrastructure with graphs</span></span>
-   <span data-ttu-id="45030-119">Registrando nomes com o PNRP</span><span class="sxs-lookup"><span data-stu-id="45030-119">Registering names with PNRP</span></span>
-   <span data-ttu-id="45030-120">Resolvendo nomes com o PNRP</span><span class="sxs-lookup"><span data-stu-id="45030-120">Resolving names with PNRP</span></span>
-   <span data-ttu-id="45030-121">Cancelando o registro de nomes com o PNRP</span><span class="sxs-lookup"><span data-stu-id="45030-121">Unregistering names with PNRP</span></span>

## <a name="group-chat"></a><span data-ttu-id="45030-122">Chat de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-122">Group Chat</span></span>

<span data-ttu-id="45030-123">O aplicativo de exemplo de chat de grupo é um aplicativo de chat simples que demonstra como usar as APIs de agrupamento de pares e do Identity Manager.</span><span class="sxs-lookup"><span data-stu-id="45030-123">The Group Chat sample application is a simple chat application that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="45030-124">O aplicativo demonstra as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="45030-124">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="45030-125">Criando uma identidade</span><span class="sxs-lookup"><span data-stu-id="45030-125">Creating an identity</span></span>
-   <span data-ttu-id="45030-126">Criando e obtendo informações de identidade</span><span class="sxs-lookup"><span data-stu-id="45030-126">Creating and obtaining identity information</span></span>
-   <span data-ttu-id="45030-127">Enumerando identidades</span><span class="sxs-lookup"><span data-stu-id="45030-127">Enumerating identities</span></span>
-   <span data-ttu-id="45030-128">Enumerando grupos associados a uma identidade</span><span class="sxs-lookup"><span data-stu-id="45030-128">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="45030-129">Creating a group</span><span class="sxs-lookup"><span data-stu-id="45030-129">Creating a group</span></span>
-   <span data-ttu-id="45030-130">Criando convites para um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-130">Creating invitations for a group</span></span>
-   <span data-ttu-id="45030-131">Conectando a um grupo existente</span><span class="sxs-lookup"><span data-stu-id="45030-131">Connecting to an existing group</span></span>
-   <span data-ttu-id="45030-132">Desconectando de um grupo existente</span><span class="sxs-lookup"><span data-stu-id="45030-132">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="45030-133">Extraindo informações das propriedades do grupo</span><span class="sxs-lookup"><span data-stu-id="45030-133">Extracting information from the group properties</span></span>
-   <span data-ttu-id="45030-134">Usando conexões diretas com um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-134">Using direct connections with a group</span></span>
-   <span data-ttu-id="45030-135">Usando as funções de enumeração dentro de um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-135">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="45030-136">Enumerando membros do grupo</span><span class="sxs-lookup"><span data-stu-id="45030-136">Enumerating group members</span></span>
-   <span data-ttu-id="45030-137">Adicionando registros a um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-137">Adding records to a group</span></span>
-   <span data-ttu-id="45030-138">Usando a notificação e a infraestrutura de eventos com grupos</span><span class="sxs-lookup"><span data-stu-id="45030-138">Using the notification and event infrastructure with groups</span></span>

## <a name="group-browser"></a><span data-ttu-id="45030-139">Navegador de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-139">Group Browser</span></span>

<span data-ttu-id="45030-140">O aplicativo de exemplo navegador de grupo é uma ferramenta de gerenciamento de grupo par simples que demonstra como usar as APIs de agrupamento de pares e Gerenciador de identidades.</span><span class="sxs-lookup"><span data-stu-id="45030-140">The Group Browser sample application is a simple peer group management tool that demonstrates how to use the Peer Grouping and Identity Manager APIs.</span></span> <span data-ttu-id="45030-141">O aplicativo demonstra as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="45030-141">The application demonstrates the following tasks:</span></span>

-   <span data-ttu-id="45030-142">Enumerando nuvens PNRP</span><span class="sxs-lookup"><span data-stu-id="45030-142">Enumerating PNRP clouds</span></span>
-   <span data-ttu-id="45030-143">Enumerando identidades</span><span class="sxs-lookup"><span data-stu-id="45030-143">Enumerating identities</span></span>
-   <span data-ttu-id="45030-144">Enumerando grupos associados a uma identidade</span><span class="sxs-lookup"><span data-stu-id="45030-144">Enumerating groups associated with an identity</span></span>
-   <span data-ttu-id="45030-145">Criando e excluindo identidades</span><span class="sxs-lookup"><span data-stu-id="45030-145">Creating and deleting identities</span></span>
-   <span data-ttu-id="45030-146">Criando um grupo e associando-o a uma identidade</span><span class="sxs-lookup"><span data-stu-id="45030-146">Creating a group and associating it with an identity</span></span>
-   <span data-ttu-id="45030-147">Criando um convite e salvando-o</span><span class="sxs-lookup"><span data-stu-id="45030-147">Creating an invitation and saving it</span></span>
-   <span data-ttu-id="45030-148">Abrindo um convite e usando-o para ingressar em um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-148">Opening an invitation and using it to join a group</span></span>
-   <span data-ttu-id="45030-149">Excluindo uma identidade e uma associação de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-149">Deleting an identity and group membership</span></span>
-   <span data-ttu-id="45030-150">Conectando a um grupo existente</span><span class="sxs-lookup"><span data-stu-id="45030-150">Connecting to an existing group</span></span>
-   <span data-ttu-id="45030-151">Desconectando de um grupo existente</span><span class="sxs-lookup"><span data-stu-id="45030-151">Disconnecting from an existing group</span></span>
-   <span data-ttu-id="45030-152">Extraindo informações de propriedades de grupo</span><span class="sxs-lookup"><span data-stu-id="45030-152">Extracting information from group properties</span></span>
-   <span data-ttu-id="45030-153">Usando as funções de enumeração dentro de um grupo</span><span class="sxs-lookup"><span data-stu-id="45030-153">Using the enumeration functions within a group</span></span>
-   <span data-ttu-id="45030-154">Enumerando membros do grupo</span><span class="sxs-lookup"><span data-stu-id="45030-154">Enumerating group members</span></span>
-   <span data-ttu-id="45030-155">Usando a notificação e a infraestrutura de eventos com grupos</span><span class="sxs-lookup"><span data-stu-id="45030-155">Using the notification and event infrastructure with groups</span></span>

 

 



