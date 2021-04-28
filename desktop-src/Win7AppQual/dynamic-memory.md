---
description: Memória Dinâmica
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Memória Dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088464"
---
# <a name="dynamic-memory"></a><span data-ttu-id="0c5bd-103">Memória Dinâmica</span><span class="sxs-lookup"><span data-stu-id="0c5bd-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0c5bd-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="0c5bd-104">Affected Platforms</span></span>

<span data-ttu-id="0c5bd-105">**Clientes (em execução como máquinas virtuais)** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c5bd-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="0c5bd-106">**Servidores** -Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="0c5bd-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="0c5bd-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="0c5bd-107">Feature Impact</span></span>

 <span data-ttu-id="0c5bd-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="0c5bd-108">**Severity** - Low</span></span>  
<span data-ttu-id="0c5bd-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="0c5bd-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="0c5bd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c5bd-110">Description</span></span>

<span data-ttu-id="0c5bd-111">Em um alto nível, o Hyper-V Memória Dinâmica é um aprimoramento de gerenciamento de memória para a função do Hyper-V incluída no Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="0c5bd-112">Ele foi projetado para uso em produção e permite que os clientes alcancem taxas de maior capacidade de consolidação/VM (máquina virtual), otimizando a utilização de memória no computador físico.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="0c5bd-113">A alocação de memória estática é reduzida e a memória adicional é alocada de acordo com a necessidade.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="0c5bd-114">Memória Dinâmica afeta os desenvolvedores de software que desejam garantir que o software funcione corretamente em um ambiente de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="0c5bd-115">Cenário de uso</span><span class="sxs-lookup"><span data-stu-id="0c5bd-115">Usage Scenario</span></span>

<span data-ttu-id="0c5bd-116">Há dois cenários de uso principal em que Memória Dinâmica entram em cena, aplicativos do lado do host e aplicativos do lado do convidado.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="0c5bd-117">**Aplicativos do lado do host (ferramentas de gerenciamento)**</span><span class="sxs-lookup"><span data-stu-id="0c5bd-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="0c5bd-118">As ferramentas antigas que gerenciam um novo servidor Windows Server 2008 R2 SP1 não poderão acessar as novas configurações de Memória Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="0c5bd-119">Novas APIs e contadores de desempenho do WMI foram desenvolvidos para gerenciar as novas configurações de Memória Dinâmica para máquinas virtuais do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="0c5bd-120">Os desenvolvedores de software que trabalham em ferramentas de gerenciamento devem aproveitar essas APIs e contadores para uso com o Windows Server 2008 R2 SP1 com a função Hyper-V instalada.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="0c5bd-121">Os detalhes sobre essas novas APIs estarão disponíveis por meio [da documentação do provedor WMI do Hyper-V no MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span><span class="sxs-lookup"><span data-stu-id="0c5bd-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="0c5bd-122">**Aplicativos do lado do convidado**</span><span class="sxs-lookup"><span data-stu-id="0c5bd-122">**Guest-side applications**</span></span>

<span data-ttu-id="0c5bd-123">Os desenvolvedores que escrevem software para uso dentro de uma máquina virtual configurada para usar Memória Dinâmica precisam ter em mente que a memória do sistema de VM não é mais constante.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="0c5bd-124">Consequentemente, o aplicativo deve liberar memória quando não for mais necessário para permitir que outros aplicativos tirem proveito do recurso.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="0c5bd-125">Alocações de memória e desalocações continuam funcionando normalmente para aplicativos de usuário.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="0c5bd-126">Memória Dinâmica é completamente transparente para a maioria dos aplicativos do usuário final.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="0c5bd-127">No entanto, se o software que está sendo desenvolvido fizer uso de contadores de desempenho de memória na máquina virtual, o teste cuidadoso deverá ser executado em um ambiente Memória Dinâmica habilitado para garantir que o software faça as alterações feitas na conta da alocação de memória do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="0c5bd-128">A memória disponível não é mais "estática" da perspectiva da máquina virtual? s.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="0c5bd-129">Soluções</span><span class="sxs-lookup"><span data-stu-id="0c5bd-129">Solutions</span></span>

<span data-ttu-id="0c5bd-130">As máquinas virtuais devem ter o SP1 (Integration Services) atualizado instalado a fim de aproveitar o Memória Dinâmica.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="0c5bd-131">Verifique se todos os computadores usados no gerenciamento de máquinas virtuais do Hyper-V estão usando os bits mais recentes do Windows Server 2008 R2 SP1.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="0c5bd-132">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="0c5bd-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="0c5bd-133">Memória Dinâmica entrando no blog do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="0c5bd-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="0c5bd-134">Usando o provedor WMI do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="0c5bd-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="0c5bd-135">Isenção de responsabilidade</span><span class="sxs-lookup"><span data-stu-id="0c5bd-135">Disclaimer</span></span>

<span data-ttu-id="0c5bd-136">As informações contidas neste documento estão relacionadas ao produto de pré-lançamento software que pode ser substancialmente modificado antes de sua primeira versão comercial.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="0c5bd-137">De acordo, as informações podem não descrever ou refletir com precisão o produto de software quando o primeiro é lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="0c5bd-138">Este documento serve apenas para fins informativos.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-138">This document is for informational purposes only.</span></span> <span data-ttu-id="0c5bd-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="0c5bd-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
