---
title: Plataforma de filtragem do Windows
description: A WFP (Windows Filtering Platform) é um conjunto de API e serviços do sistema que fornecem uma plataforma para a criação de aplicativos de filtragem de rede.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Plataforma de filtragem do Windows
- Página inicial da plataforma de filtragem do Windows, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105766917"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="1851b-105">Plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="1851b-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="1851b-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="1851b-106">Purpose</span></span>

<span data-ttu-id="1851b-107">A WFP (Windows Filtering Platform) é um conjunto de API e serviços do sistema que fornecem uma plataforma para a criação de aplicativos de filtragem de rede.</span><span class="sxs-lookup"><span data-stu-id="1851b-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="1851b-108">A API da WFP permite aos desenvolvedores escrever código que interaja com o processamento de pacote que acontece em diversos níveis na pilha de rede do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1851b-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="1851b-109">Os dados de rede podem ser filtrados e também modificados antes de atingirem seu destino.</span><span class="sxs-lookup"><span data-stu-id="1851b-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="1851b-110">Ao fornecer uma plataforma de desenvolvimento mais simples, a WFP foi projetada para substituir as tecnologias de filtragem de pacotes anteriores, como filtros interface do driver de transporte (TDI), filtros de NDIS (especificação de interface de driver de rede) e LSP (provedores de serviço em camadas) do Winsock.</span><span class="sxs-lookup"><span data-stu-id="1851b-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="1851b-111">A partir do Windows Server 2008 e do Windows Vista, o cabo de firewall e os drivers de conexão de filtro não estão disponíveis; em vez disso, os aplicativos que estavam usando esses drivers devem usar a WFP.</span><span class="sxs-lookup"><span data-stu-id="1851b-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="1851b-112">Com a API WFP, os desenvolvedores podem implementar firewalls, sistemas de detecção de intrusão, programas antivírus, ferramentas de monitoramento de rede e controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="1851b-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="1851b-113">A WFP integra-se ao e fornece suporte para recursos de firewall, como comunicação autenticada e configuração dinâmica de firewall com base no uso dos aplicativos da API de soquetes (política baseada em aplicativo).</span><span class="sxs-lookup"><span data-stu-id="1851b-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="1851b-114">A WFP também fornece infraestrutura para gerenciamento de política IPsec, notificações de alteração, diagnóstico de rede e filtragem com monitoração de estado.</span><span class="sxs-lookup"><span data-stu-id="1851b-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="1851b-115">A plataforma de filtragem do Windows é uma plataforma de desenvolvimento e não um firewall em si.</span><span class="sxs-lookup"><span data-stu-id="1851b-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="1851b-116">O aplicativo de firewall criado no Windows Vista, no Windows Server 2008 e em sistemas operacionais posteriores do firewall do Windows com segurança avançada (WFAS) é implementado usando o WFP.</span><span class="sxs-lookup"><span data-stu-id="1851b-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="1851b-117">Portanto, os aplicativos desenvolvidos com a API WFP ou a [API do WFAS](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) usam a lógica de arbitragem de filtragem comum que é incorporada à WFP.</span><span class="sxs-lookup"><span data-stu-id="1851b-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="1851b-118">A API WFP consiste em uma API do modo de usuário e uma API do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="1851b-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="1851b-119">Esta seção fornece uma visão geral de toda a WFP e descreve em detalhes apenas a parte do modo de usuário da API WFP.</span><span class="sxs-lookup"><span data-stu-id="1851b-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="1851b-120">Para obter uma descrição detalhada da API WFP do modo kernel, consulte a ajuda online do [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="1851b-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1851b-121">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="1851b-121">Developer audience</span></span>

<span data-ttu-id="1851b-122">A API da plataforma de filtragem do Windows foi projetada para uso por programadores que usam o software de desenvolvimento C/C++.</span><span class="sxs-lookup"><span data-stu-id="1851b-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="1851b-123">Os programadores devem estar familiarizados com os conceitos de rede e o design de sistemas usando componentes de modo de usuário e de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="1851b-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1851b-124">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="1851b-124">Run-time requirements</span></span>

<span data-ttu-id="1851b-125">A plataforma de filtragem do Windows tem suporte em clientes que executam o Windows Vista e posterior e em servidores que executam o Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1851b-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="1851b-126">Para obter informações sobre os requisitos de tempo de execução para um elemento de programação específico, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="1851b-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="1851b-127">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1851b-127">In this section</span></span>



| <span data-ttu-id="1851b-128">Tópico</span><span class="sxs-lookup"><span data-stu-id="1851b-128">Topic</span></span>                                                                                               | <span data-ttu-id="1851b-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="1851b-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1851b-130">O que há de novo na plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="1851b-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="1851b-131">Informações sobre novos recursos e APIs na plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="1851b-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="1851b-132">Sobre a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="1851b-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1851b-133">Uma visão geral da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="1851b-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="1851b-134">Usando a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="1851b-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="1851b-135">Código de exemplo usando a API da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="1851b-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="1851b-136">Referência da API da plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="1851b-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="1851b-137">Documentação para as funções, estruturas e constantes da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="1851b-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="1851b-138">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1851b-138">Additional resources</span></span>

<span data-ttu-id="1851b-139">Para fazer perguntas e ter discussões sobre como usar a API WFP, visite o [Fórum da plataforma de filtragem do Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="1851b-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1851b-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1851b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1851b-141">API da plataforma de filtragem do Windows no modo kernel-guia de design</span><span class="sxs-lookup"><span data-stu-id="1851b-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="1851b-142">API da plataforma de filtragem do Windows no modo kernel-referência</span><span class="sxs-lookup"><span data-stu-id="1851b-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="1851b-143">Firewall do Windows com Advanced Security</span><span class="sxs-lookup"><span data-stu-id="1851b-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="1851b-144">Classe auxiliar extensível do diagnóstico WFP</span><span class="sxs-lookup"><span data-stu-id="1851b-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="1851b-145">Extensões do Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="1851b-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

