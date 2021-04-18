---
title: Sobre a plataforma de filtragem do Windows
description: A WFP (Windows Filtering Platform) é uma plataforma de processamento de tráfego de rede projetada para substituir as interfaces de filtragem de tráfego de rede do Windows XP e do Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105753486"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="76f1f-103">Sobre a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="76f1f-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="76f1f-104">A WFP (Windows Filtering Platform) é uma plataforma de processamento de tráfego de rede projetada para substituir as interfaces de filtragem de tráfego de rede do Windows XP e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76f1f-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="76f1f-105">A WFP consiste em um conjunto de ganchos na pilha de rede e em um mecanismo de filtragem que coordena as interações de pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="76f1f-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="76f1f-106">Os componentes de WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="76f1f-107">Mecanismo de filtro</span><span class="sxs-lookup"><span data-stu-id="76f1f-107">Filter Engine</span></span>

<span data-ttu-id="76f1f-108">A principal infraestrutura de filtragem de várias camadas, hospedada no modo kernel e no modo de usuário, que substitui os vários módulos de filtragem no subsistema de rede do Windows XP e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="76f1f-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="76f1f-109">Filtra o tráfego de rede em qualquer camada do sistema em qualquer campo de dados que um Shim possa fornecer.</span><span class="sxs-lookup"><span data-stu-id="76f1f-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="76f1f-110">Implementa os filtros de "texto explicativo" invocando os textos explicativos durante a classificação.</span><span class="sxs-lookup"><span data-stu-id="76f1f-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="76f1f-111">Retorna as ações "permitir" ou "bloquear" para o Shim que a invocou para imposição.</span><span class="sxs-lookup"><span data-stu-id="76f1f-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="76f1f-112">Fornece arbitragem entre diferentes fontes de política.</span><span class="sxs-lookup"><span data-stu-id="76f1f-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="76f1f-113">Por exemplo, determina a prioridade quando um aplicativo é configurado para proteger qualquer tráfego de rede relacionado a ele, mas o firewall local é configurado para impedir o tráfego protegido do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="76f1f-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="76f1f-114">Mecanismo de filtragem base (BFE)</span><span class="sxs-lookup"><span data-stu-id="76f1f-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="76f1f-115">Um serviço que controla a operação da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="76f1f-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="76f1f-116">Ele executa as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="76f1f-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="76f1f-117">Aceita filtros e outras definições de configuração para a plataforma.</span><span class="sxs-lookup"><span data-stu-id="76f1f-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="76f1f-118">Relata o estado atual do sistema, incluindo estatísticas.</span><span class="sxs-lookup"><span data-stu-id="76f1f-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="76f1f-119">Impõe o modelo de segurança para aceitar a configuração na plataforma.</span><span class="sxs-lookup"><span data-stu-id="76f1f-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="76f1f-120">Por exemplo, um administrador local pode adicionar filtros, mas outros usuários só podem exibi-los.</span><span class="sxs-lookup"><span data-stu-id="76f1f-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="76f1f-121">Direciona definições de configuração para outros módulos no sistema.</span><span class="sxs-lookup"><span data-stu-id="76f1f-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="76f1f-122">Por exemplo, as políticas de negociação de IPsec vão para módulos de chaveamento IKE/AuthIP, filtros acessam o mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="76f1f-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="76f1f-123">Shims</span><span class="sxs-lookup"><span data-stu-id="76f1f-123">Shims</span></span>

<span data-ttu-id="76f1f-124">Componentes do modo kernel que residem entre a pilha de rede e o mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="76f1f-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="76f1f-125">Os shims fazem a decisão de filtragem classificando em relação ao mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="76f1f-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="76f1f-126">A seguir está uma lista de shims disponíveis.</span><span class="sxs-lookup"><span data-stu-id="76f1f-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="76f1f-127">Shim de aplicação da camada de aplicativo (EPA).</span><span class="sxs-lookup"><span data-stu-id="76f1f-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="76f1f-128">Shim do módulo da camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="76f1f-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="76f1f-129">Shim do módulo da camada de rede.</span><span class="sxs-lookup"><span data-stu-id="76f1f-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="76f1f-130">Shim de erro do protocolo ICMP.</span><span class="sxs-lookup"><span data-stu-id="76f1f-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="76f1f-131">Descartar Shim.</span><span class="sxs-lookup"><span data-stu-id="76f1f-131">Discard shim.</span></span>
-   <span data-ttu-id="76f1f-132">Shim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="76f1f-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="76f1f-133">Textos explicativos</span><span class="sxs-lookup"><span data-stu-id="76f1f-133">Callouts</span></span>

<span data-ttu-id="76f1f-134">Conjunto de funções expostas por um driver e usadas para filtragem especializada.</span><span class="sxs-lookup"><span data-stu-id="76f1f-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="76f1f-135">Além das ações básicas de "permitir" e "bloquear", os textos explicativos podem modificar e proteger o tráfego de rede de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="76f1f-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="76f1f-136">Consulte o tópico [drivers de texto explicativo da plataforma de filtragem do Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) na documentação do Windows Driver Kit (WDK) para obter mais informações sobre textos explicativos.</span><span class="sxs-lookup"><span data-stu-id="76f1f-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="76f1f-137">A WFP fornece textos explicativos internos que realizam as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="76f1f-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="76f1f-138">Execute o processamento IPsec.</span><span class="sxs-lookup"><span data-stu-id="76f1f-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="76f1f-139">Ajuste o comportamento de filtragem com estado.</span><span class="sxs-lookup"><span data-stu-id="76f1f-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="76f1f-140">Execute a filtragem de modo furtivo (queda silenciosa de pacotes que não foram solicitados).</span><span class="sxs-lookup"><span data-stu-id="76f1f-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="76f1f-141">Controle o descarregamento de Chimney TCP.</span><span class="sxs-lookup"><span data-stu-id="76f1f-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="76f1f-142">Interaja com o serviço Teredo.</span><span class="sxs-lookup"><span data-stu-id="76f1f-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="76f1f-143">O mecanismo de filtro permite que os textos explicativos de terceiros se registrem em cada uma de suas camadas de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="76f1f-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="76f1f-144">Interface de programação de aplicativo</span><span class="sxs-lookup"><span data-stu-id="76f1f-144">Application Programming Interface</span></span>

<span data-ttu-id="76f1f-145">Um conjunto de tipos de dados e funções disponíveis aos desenvolvedores para criar e gerenciar aplicativos de filtragem de rede.</span><span class="sxs-lookup"><span data-stu-id="76f1f-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="76f1f-146">Esses tipos de dados e funções são agrupados em vários [conjuntos de API](api-sets.md).</span><span class="sxs-lookup"><span data-stu-id="76f1f-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="76f1f-147">Recursos de WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-147">WFP Features</span></span>

-   <span data-ttu-id="76f1f-148">Fornece uma infraestrutura de filtragem de pacotes em que os ISVs (fornecedores independentes de software) podem conectar módulos de filtragem especializados.</span><span class="sxs-lookup"><span data-stu-id="76f1f-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="76f1f-149">Funciona com IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="76f1f-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="76f1f-150">Permite filtragem, modificação e reinjeção de dados.</span><span class="sxs-lookup"><span data-stu-id="76f1f-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="76f1f-151">Executa o processamento de pacotes e de fluxo.</span><span class="sxs-lookup"><span data-stu-id="76f1f-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="76f1f-152">Permite que a filtragem de pacotes seja habilitada por aplicativo, por usuário e por conexão, além de por interface de rede ou por porta.</span><span class="sxs-lookup"><span data-stu-id="76f1f-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="76f1f-153">Fornece segurança de tempo de inicialização até que o BFE (mecanismo de filtragem base) possa ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="76f1f-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="76f1f-154">Habilita a filtragem de conexão com estado.</span><span class="sxs-lookup"><span data-stu-id="76f1f-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="76f1f-155">Manipula dados de pré e pós-criptografados por IPsec.</span><span class="sxs-lookup"><span data-stu-id="76f1f-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="76f1f-156">Permite a integração de políticas de filtragem de firewall e IPsec.</span><span class="sxs-lookup"><span data-stu-id="76f1f-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="76f1f-157">Fornece uma infraestrutura de gerenciamento de política para determinar quando filtros específicos devem ser ativados.</span><span class="sxs-lookup"><span data-stu-id="76f1f-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="76f1f-158">Isso inclui a mediação de requisitos conflitantes de vários filtros fornecidos por diferentes fornecedores.</span><span class="sxs-lookup"><span data-stu-id="76f1f-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="76f1f-159">Lida com a maior parte da remontagem de pacotes e o controle de estado.</span><span class="sxs-lookup"><span data-stu-id="76f1f-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="76f1f-160">Inclui um sistema de notificação de usuário genérico que informa os assinantes de alterações no sistema de filtragem.</span><span class="sxs-lookup"><span data-stu-id="76f1f-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="76f1f-161">Implementa funções de enumeração que relatam o estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="76f1f-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="76f1f-162">Usa eventos de rede para registrar erros de IPsec e quedas de pacotes.</span><span class="sxs-lookup"><span data-stu-id="76f1f-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="76f1f-163">Dá suporte a uma [classe auxiliar NDF (](/windows/desktop/NDF/extensible-helper-classes)estrutura de diagnóstico de rede).</span><span class="sxs-lookup"><span data-stu-id="76f1f-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="76f1f-164">O oferece suporte às [extensões de soquete seguro](/windows/desktop/WinSock/winsock-secure-socket-extensions) para a API do Winsock, o que permite que os aplicativos de rede protejam seu tráfego configurando a WFP.</span><span class="sxs-lookup"><span data-stu-id="76f1f-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="76f1f-165">Em camadas de aplicação de camada de aplicativo (ALE), afeta minimamente o desempenho da rede processando apenas o primeiro pacote em uma conexão.</span><span class="sxs-lookup"><span data-stu-id="76f1f-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="76f1f-166">Integra o descarregamento de hardware em que os módulos de texto explicativo em modo kernel podem usar o hardware para executar uma inspeção de pacote específica.</span><span class="sxs-lookup"><span data-stu-id="76f1f-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76f1f-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76f1f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f1f-168">Arquitetura WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="76f1f-169">Operação WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="76f1f-170">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="76f1f-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="76f1f-171">Configuração de IPsec</span><span class="sxs-lookup"><span data-stu-id="76f1f-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="76f1f-172">Configuração de WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="76f1f-173">Monitoramento de WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="76f1f-174">API WFP</span><span class="sxs-lookup"><span data-stu-id="76f1f-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

