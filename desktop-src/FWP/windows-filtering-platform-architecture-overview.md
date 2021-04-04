---
title: Arquitetura WFP
description: Esta seção fornece uma breve visão geral da arquitetura da plataforma de filtragem do Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162232"
---
# <a name="wfp-architecture"></a><span data-ttu-id="757b7-103">Arquitetura WFP</span><span class="sxs-lookup"><span data-stu-id="757b7-103">WFP Architecture</span></span>

<span data-ttu-id="757b7-104">A figura a seguir mostra a arquitetura básica da WFP (Windows Filtering Platform).</span><span class="sxs-lookup"><span data-stu-id="757b7-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![arquitetura básica do diagrama da plataforma de filtragem do Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="757b7-106">Mecanismo de filtro</span><span class="sxs-lookup"><span data-stu-id="757b7-106">Filter Engine</span></span>

<span data-ttu-id="757b7-107">O mecanismo de filtro contém um componente de modo de usuário e um componente de modo kernel, que juntos executam todas as operações de filtragem em dados de rede.</span><span class="sxs-lookup"><span data-stu-id="757b7-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="757b7-108">O mecanismo de filtro contém várias camadas de filtragem que são mapeadas livremente para as camadas de pilha de rede do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="757b7-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="757b7-109">As camadas do mecanismo de filtro são divididas em camadas de modo de usuário e camadas de modo kernel com base no componente do mecanismo de filtro que as possui.</span><span class="sxs-lookup"><span data-stu-id="757b7-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="757b7-110">O componente do modo de usuário executa a filtragem de RPC e IPsec.</span><span class="sxs-lookup"><span data-stu-id="757b7-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="757b7-111">O mecanismo de filtro contém aproximadamente 10 camadas de filtragem de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="757b7-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="757b7-112">O componente do modo kernel executa a filtragem nas camadas de rede e de transporte da pilha de TC/IP.</span><span class="sxs-lookup"><span data-stu-id="757b7-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="757b7-113">Esse componente também chama as funções de texto explicativo disponíveis durante o processo de [classificação](basic-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="757b7-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="757b7-114">O mecanismo de filtro contém aproximadamente 50 camadas de filtragem de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="757b7-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="757b7-115">Consulte [**Filtrar identificadores de camada**](management-filtering-layer-identifiers-.md) para obter uma descrição de cada uma das camadas do mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="757b7-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="757b7-116">Mecanismo de Filtragem Base</span><span class="sxs-lookup"><span data-stu-id="757b7-116">Base Filtering Engine</span></span>

<span data-ttu-id="757b7-117">O BFE (mecanismo de filtragem base) é um serviço de modo de usuário (bfe.dll em execução em um processo de svchost.exe) que coordena os componentes da WFP.</span><span class="sxs-lookup"><span data-stu-id="757b7-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="757b7-118">As tarefas principais executadas pelo BFE são adicionar e remover filtros do sistema, armazenar a configuração de filtro e impor a segurança de configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="757b7-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="757b7-119">Os aplicativos se comunicam com o BFE por meio das [funções de gerenciamento de WFP](fwp-mgmt-functions.md).</span><span class="sxs-lookup"><span data-stu-id="757b7-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="757b7-120">Drivers de texto explicativo</span><span class="sxs-lookup"><span data-stu-id="757b7-120">Callout Drivers</span></span>

<span data-ttu-id="757b7-121">Os drivers de texto explicativo fornecem funcionalidade de filtragem adicional adicionando funções de texto explicativo personalizadas ao mecanismo de filtro em uma ou mais das camadas de filtragem do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="757b7-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="757b7-122">Os textos explicativos dão suporte a inspeção e pacote profundos, bem como à modificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="757b7-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="757b7-123">Depois que um driver de texto explicativo tiver adicionado suas funções de texto explicativo ao mecanismo de filtro, os filtros que especificam uma função de texto explicativo de um determinado driver poderão ser adicionados ao processo de filtragem.</span><span class="sxs-lookup"><span data-stu-id="757b7-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="757b7-124">Esses filtros podem ser adicionados por um aplicativo de gerenciamento de modo de usuário ou pelo próprio driver de texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="757b7-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="757b7-125">A interface do modo kernel, fornecida no kit de desenvolvimento do Windows, só deve ser usada quando necessário e não como um substituto para a API do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="757b7-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="757b7-126">Para obter mais informações sobre drivers de texto explicativo, consulte a seção Windows Filtering Platform do [Kit de desenvolvimento do Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="757b7-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="757b7-127">A plataforma de filtragem do Windows inclui uma série de funções de texto explicativo internas que podem ser usadas para comunicação de dados segura IPsec, configurações de filtragem com estado e filtragem de modo furtivo.</span><span class="sxs-lookup"><span data-stu-id="757b7-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="757b7-128">Consulte [**identificadores de texto explicativo interno**](built-in-callout-identifiers.md) para obter uma lista completa de funções de texto explicativo internas.</span><span class="sxs-lookup"><span data-stu-id="757b7-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="757b7-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="757b7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="757b7-130">Modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="757b7-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="757b7-131">Operação WFP</span><span class="sxs-lookup"><span data-stu-id="757b7-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="757b7-132">Drivers de texto explicativo da plataforma de filtragem do Windows – guia de design</span><span class="sxs-lookup"><span data-stu-id="757b7-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="757b7-133">Drivers de texto explicativo da plataforma de filtragem do Windows-referência</span><span class="sxs-lookup"><span data-stu-id="757b7-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 