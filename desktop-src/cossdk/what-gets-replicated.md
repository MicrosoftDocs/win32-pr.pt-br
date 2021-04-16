---
description: O que é replicado
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: O que é replicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765751"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="be4a4-103">O que é replicado</span><span class="sxs-lookup"><span data-stu-id="be4a4-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="be4a4-104">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="be4a4-104">Applications</span></span>

<span data-ttu-id="be4a4-105">Todos os aplicativos instalados no computador de origem são replicados, exceto os seguintes:</span><span class="sxs-lookup"><span data-stu-id="be4a4-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="be4a4-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Elementos e dependências não-COM + de aplicativo</span><span class="sxs-lookup"><span data-stu-id="be4a4-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="be4a4-107">O administrador é responsável por replicar qualquer coisa de que um aplicativo COM+ depende, mas que não faz parte apropriada do próprio aplicativo, como arquivos de dados e DLLs.</span><span class="sxs-lookup"><span data-stu-id="be4a4-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="be4a4-108">COMREPL não replicará nada fora dos elementos do aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="be4a4-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="be4a4-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Aplicativos pré-instalados COM+</span><span class="sxs-lookup"><span data-stu-id="be4a4-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="be4a4-110">Os aplicativos que são usados internamente pelo COM+ e são instalados por meio do programa de instalação do COM+ não são replicados.</span><span class="sxs-lookup"><span data-stu-id="be4a4-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="be4a4-111">Entre elas estão as seguintes:</span><span class="sxs-lookup"><span data-stu-id="be4a4-111">These include the following:</span></span>

-   <span data-ttu-id="be4a4-112">Aplicativo do sistema</span><span class="sxs-lookup"><span data-stu-id="be4a4-112">System application</span></span>
-   <span data-ttu-id="be4a4-113">Utilitários COM+</span><span class="sxs-lookup"><span data-stu-id="be4a4-113">COM+ utilities</span></span>
-   <span data-ttu-id="be4a4-114">Ouvinte de fila de mensagens mortas do QC COM+</span><span class="sxs-lookup"><span data-stu-id="be4a4-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="be4a4-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Aplicativos criados pelo IIS</span><span class="sxs-lookup"><span data-stu-id="be4a4-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="be4a4-116">Esses aplicativos não são replicados e incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="be4a4-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="be4a4-117">Aplicativos em processo do IIS</span><span class="sxs-lookup"><span data-stu-id="be4a4-117">IIS in-process applications</span></span>
-   <span data-ttu-id="be4a4-118">Utilitários do IIS</span><span class="sxs-lookup"><span data-stu-id="be4a4-118">IIS utilities</span></span>
-   <span data-ttu-id="be4a4-119">Todos os aplicativos criados para raízes virtuais isoladas ou em pool</span><span class="sxs-lookup"><span data-stu-id="be4a4-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="be4a4-120">Lista de computadores</span><span class="sxs-lookup"><span data-stu-id="be4a4-120">Computer List</span></span>

<span data-ttu-id="be4a4-121">Os computadores remotos chamados na pasta **computadores** na ferramenta de administração de serviços de componentes não serão replicados da origem para o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="be4a4-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="be4a4-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="be4a4-122">Properties</span></span>

<span data-ttu-id="be4a4-123">As seguintes propriedades de coleção **LocalComputer** são replicadas:</span><span class="sxs-lookup"><span data-stu-id="be4a4-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="be4a4-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="be4a4-124">TransactionTimeout</span></span>
-   <span data-ttu-id="be4a4-125">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="be4a4-126">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-126">DCOMEnabled</span></span>
-   <span data-ttu-id="be4a4-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="be4a4-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="be4a4-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="be4a4-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="be4a4-129">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="be4a4-130">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-130">CISEnabled</span></span>
-   <span data-ttu-id="be4a4-131">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="be4a4-132">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="be4a4-132">InternetPortsListed</span></span>
-   <span data-ttu-id="be4a4-133">DeafultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="be4a4-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="be4a4-134">Portas</span><span class="sxs-lookup"><span data-stu-id="be4a4-134">Ports</span></span>
-   <span data-ttu-id="be4a4-135">RpcProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="be4a4-135">RpcProxyEnabled</span></span>

<span data-ttu-id="be4a4-136">As seguintes propriedades de coleção **LocalComputer** não são replicadas:</span><span class="sxs-lookup"><span data-stu-id="be4a4-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="be4a4-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="be4a4-137">Description</span></span>
-   <span data-ttu-id="be4a4-138">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="be4a4-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="be4a4-139">Isroteador</span><span class="sxs-lookup"><span data-stu-id="be4a4-139">IsRouter</span></span>

<span data-ttu-id="be4a4-140">Para obter descrições das propriedades da coleção **LocalComputer** , consulte [**LocalComputer**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="be4a4-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be4a4-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be4a4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be4a4-142">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="be4a4-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="be4a4-143">Registro em log e relatório de erros</span><span class="sxs-lookup"><span data-stu-id="be4a4-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="be4a4-144">Fases de replicação</span><span class="sxs-lookup"><span data-stu-id="be4a4-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="be4a4-145">Usando COMREPL</span><span class="sxs-lookup"><span data-stu-id="be4a4-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



