---
title: Sobre Serviços de Área de Trabalho Remota
description: O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761335"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="4b808-104">Sobre Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-104">About Remote Desktop Services</span></span>

<span data-ttu-id="4b808-105">O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.</span><span class="sxs-lookup"><span data-stu-id="4b808-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="4b808-106">Cada terminal fornece um canal para entrada e saída entre um usuário e o computador host.</span><span class="sxs-lookup"><span data-stu-id="4b808-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="4b808-107">Um usuário pode fazer logon em um terminal e, em seguida, executar aplicativos no computador host, acessar arquivos, bancos de dados, recursos de rede e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4b808-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="4b808-108">Cada sessão de terminal é independente, com o sistema operacional do host que gerencia conflitos entre vários usuários que contendem recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="4b808-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="4b808-109">A principal diferença entre Serviços de Área de Trabalho Remota e o ambiente de mainframe tradicional é que os terminais inconsistentes em um ambiente de mainframe fornecem apenas entrada e saída baseadas em caractere.</span><span class="sxs-lookup"><span data-stu-id="4b808-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="4b808-110">Um cliente de Conexão de Área de Trabalho Remota (RDC) ou emulador fornece uma interface gráfica completa do usuário, incluindo uma área de trabalho do sistema operacional Windows e suporte para uma variedade de dispositivos de entrada, como um teclado e um mouse.</span><span class="sxs-lookup"><span data-stu-id="4b808-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="4b808-111">No ambiente de Serviços de Área de Trabalho Remota, um aplicativo é executado inteiramente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor de terminal).</span><span class="sxs-lookup"><span data-stu-id="4b808-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="4b808-112">O cliente RDC não executa nenhum processamento local de software de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b808-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="4b808-113">O servidor transmite a interface gráfica do usuário para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4b808-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="4b808-114">O cliente transmite a entrada do usuário de volta para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4b808-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="4b808-115">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b808-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b808-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4b808-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4b808-117">Modificar o padrão de redirecionamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4b808-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="4b808-118">Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="4b808-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-119">Protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="4b808-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="4b808-120">O protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados no Windows em execução em um servidor.</span><span class="sxs-lookup"><span data-stu-id="4b808-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-121">API de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="4b808-122">A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4b808-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-123">Serviços de Área de Trabalho Remota aplicativos de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4b808-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="4b808-124">Descreve os aplicativos de gerenciamento aos quais Serviços de Área de Trabalho Remota dá suporte.</span><span class="sxs-lookup"><span data-stu-id="4b808-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-125">Diretrizes de programação de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="4b808-126">Tópicos que fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4b808-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-127">Sessões de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="4b808-128">Como cada logon em um cliente de Conexão de Área de Trabalho Remota (RDC) recebe uma ID de sessão separada, a experiência do usuário é semelhante a ser conectada a vários computadores ao mesmo tempo; por exemplo, um computador do escritório e um computador doméstico.</span><span class="sxs-lookup"><span data-stu-id="4b808-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-129">Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="4b808-130">Descreve como instalar um Conexão Web de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4b808-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-131">Recursos em um servidor Host da Sessão da Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="4b808-132">Vários usuários podem fazer logon simultaneamente em um único servidor de Host da Sessão RD, compartilhando os recursos de hardware e software do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b808-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="4b808-133">O que há de novo no Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="4b808-134">Tópicos que descrevem as alterações em cada versão da API de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="4b808-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4b808-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b808-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b808-136">Conectar-se a outro computador usando Conexão de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="4b808-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




