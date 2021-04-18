---
title: Serviços de Área de Trabalho Remota (Serviços de Área de Trabalho Remota)
description: Área de Trabalho Remota da Microsoft Services é um software de acesso de computador remoto que dá suporte ao acesso à área de trabalho remota. Serviços de Área de Trabalho Remota conecta vários clientes a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota home page
- Serviços de terminal consulte Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105789433"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="373c8-107">Serviços de Área de Trabalho Remota (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="373c8-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="373c8-108">Finalidade</span><span class="sxs-lookup"><span data-stu-id="373c8-108">Purpose</span></span>

<span data-ttu-id="373c8-109">O Windows Server 2012 R2, o Windows Server 2012, o Windows Server 2008 R2 ou o Windows Server 2008 com Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) permitem que um servidor hospede várias sessões de cliente simultâneas.</span><span class="sxs-lookup"><span data-stu-id="373c8-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="373c8-110">Área de Trabalho Remota usa a tecnologia Serviços de Área de Trabalho Remota para permitir que uma única sessão seja executada remotamente.</span><span class="sxs-lookup"><span data-stu-id="373c8-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="373c8-111">Um usuário pode se conectar a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor de terminal) usando o software cliente do Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="373c8-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="373c8-112">A Conexão Web de Área de Trabalho Remota estende Serviços de Área de Trabalho Remota tecnologia à Web.</span><span class="sxs-lookup"><span data-stu-id="373c8-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="373c8-113">Este tópico destina-se a desenvolvedores de software.</span><span class="sxs-lookup"><span data-stu-id="373c8-113">This topic is for software developers.</span></span> <span data-ttu-id="373c8-114">Se você estiver procurando informações do usuário para Área de Trabalho Remota conexões, consulte [conexão de área de trabalho remota: perguntas](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)frequentes.</span><span class="sxs-lookup"><span data-stu-id="373c8-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="373c8-115">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="373c8-115">Where applicable</span></span>

<span data-ttu-id="373c8-116">Um cliente Conexão de Área de Trabalho Remota (RDC) pode existir em uma variedade de formulários.</span><span class="sxs-lookup"><span data-stu-id="373c8-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="373c8-117">Dispositivos de hardware de cliente fino que executam um sistema operacional incorporado baseado no Windows podem executar o software cliente do RDC para se conectar a um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="373c8-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="373c8-118">Computadores baseados em Windows, Macintosh ou UNIX podem executar o software cliente do RDC para se conectar a um servidor de Host da Sessão RD para exibir aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="373c8-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="373c8-119">Essa combinação de clientes RDC fornece acesso a aplicativos baseados no Windows de praticamente qualquer sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="373c8-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="373c8-120">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="373c8-120">Developer audience</span></span>

<span data-ttu-id="373c8-121">Os desenvolvedores que usam Serviços de Área de Trabalho Remota devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="373c8-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="373c8-122">É necessário ter familiaridade com a arquitetura de cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="373c8-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="373c8-123">O Conexão Web de Área de Trabalho Remota inclui interfaces programáveis para criar e implantar canais virtuais programáveis em Serviços de Área de Trabalho Remota aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="373c8-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="373c8-124">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="373c8-124">Run-time requirements</span></span>

<span data-ttu-id="373c8-125">Os aplicativos que usam Serviços de Área de Trabalho Remota exigem o Windows Server 2012 R2, o Windows 8.1, o Windows Server 2012, o Windows 8, o Windows Server 2008 R2, o Windows 7, o Windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="373c8-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="373c8-126">Para usar Conexão Web de Área de Trabalho Remota funcionalidade, o aplicativo cliente Serviços de Área de Trabalho Remota requer o Internet Explorer e uma conexão com o World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="373c8-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="373c8-127">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="373c8-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="373c8-128">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="373c8-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="373c8-129">Área de Trabalho Remota controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="373c8-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="373c8-130">Descreve como usar o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="373c8-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-131">API do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="373c8-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="373c8-132">Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.</span><span class="sxs-lookup"><span data-stu-id="373c8-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-133">Canais virtuais Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="373c8-134">Os *canais virtuais* são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="373c8-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-135">API de redirecionamento de mídia do RemoteFX</span><span class="sxs-lookup"><span data-stu-id="373c8-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="373c8-136">A API de redirecionamento de mídia do RemoteFX é usada em uma sessão de Área de Trabalho Remota para identificar áreas do servidor que estão exibindo conteúdo de alteração rápida, como vídeo.</span><span class="sxs-lookup"><span data-stu-id="373c8-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="373c8-137">Esse conteúdo pode então ser codificado em vídeo e enviado ao cliente em formato codificado.</span><span class="sxs-lookup"><span data-stu-id="373c8-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-138">API de cliente do agente de Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="373c8-139">Descreve como usar a API de cliente do agente do Conexão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="373c8-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-140">Referência de API do agente de tarefa de área de trabalho pessoal</span><span class="sxs-lookup"><span data-stu-id="373c8-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="373c8-141">A API do agente de tarefa de área de trabalho pessoal é usada para lidar com atualizações agendadas em uma área de trabalho virtual pessoal.</span><span class="sxs-lookup"><span data-stu-id="373c8-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-142">Sobre Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="373c8-143">O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.</span><span class="sxs-lookup"><span data-stu-id="373c8-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-144">Provedor de serviços de gerenciamento de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="373c8-145">O provedor de serviços de gerenciamento de Área de Trabalho Remota (RDMS) gerencia ambientes de VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="373c8-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-146">Referência de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="373c8-147">Documentação dos métodos de propriedade que você pode usar para examinar e configurar Serviços de Área de Trabalho Remota Propriedades de usuário.</span><span class="sxs-lookup"><span data-stu-id="373c8-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="373c8-148">Serviços de Área de Trabalho Remota funções, estruturas e Conexão Web de Área de Trabalho Remota interfaces programáveis por script também são documentadas.</span><span class="sxs-lookup"><span data-stu-id="373c8-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-149">Teclas de atalho Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="373c8-150">Uma lista de teclas de atalho Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="373c8-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-151">Provedor WMI de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="373c8-152">O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.</span><span class="sxs-lookup"><span data-stu-id="373c8-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="373c8-153">Usando Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="373c8-154">Como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="373c8-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="373c8-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="373c8-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="373c8-156">Os serviços de terminal agora estão Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="373c8-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




