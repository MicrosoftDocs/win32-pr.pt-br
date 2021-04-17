---
title: Protocolo RDP
description: O protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados no Windows em execução em um servidor.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota protocolo RDP (RDP)
- RDP (consulte protocolo RDP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760123"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="50080-105">Protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="50080-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="50080-106">O protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados no Windows em execução em um servidor.</span><span class="sxs-lookup"><span data-stu-id="50080-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="50080-107">O RDP foi projetado para dar suporte a diferentes tipos de topologias de rede e vários protocolos de LAN.</span><span class="sxs-lookup"><span data-stu-id="50080-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="50080-108">Este tópico destina-se a desenvolvedores de software.</span><span class="sxs-lookup"><span data-stu-id="50080-108">This topic is for software developers.</span></span> <span data-ttu-id="50080-109">Se você estiver procurando informações do usuário para Área de Trabalho Remota, consulte [suporte do Windows](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="50080-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="50080-110">Se você estiver procurando informações de profissionais de ti para Área de Trabalho Remota, consulte [serviços de área de trabalho remota no TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="50080-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="50080-111">Arquitetura básica</span><span class="sxs-lookup"><span data-stu-id="50080-111">Basic Architecture</span></span>

<span data-ttu-id="50080-112">O RDP se baseia em, e uma extensão da, a família de protocolos ITU T. 120.</span><span class="sxs-lookup"><span data-stu-id="50080-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="50080-113">O RDP é um protocolo compatível com vários canais que permite canais virtuais separados para a realização de comunicação do dispositivo e dados de apresentação do servidor, bem como dados de teclado e mouse do cliente criptografados.</span><span class="sxs-lookup"><span data-stu-id="50080-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="50080-114">O RDP fornece uma base extensível e dá suporte a até 64.000 canais separados para transmissão de dados e provisões para transmissão do MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="50080-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="50080-115">No servidor, o RDP usa seu próprio driver de vídeo para renderizar a saída de exibição, construindo as informações de renderização em pacotes de rede usando o protocolo RDP e enviando-as pela rede para o cliente.</span><span class="sxs-lookup"><span data-stu-id="50080-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="50080-116">No cliente, o RDP recebe dados de renderização e interpreta os pacotes em chamadas de API de GDI (interface gráfica de dispositivo) do Microsoft Windows correspondentes.</span><span class="sxs-lookup"><span data-stu-id="50080-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="50080-117">Para o caminho de entrada, os eventos de teclado e mouse do cliente são redirecionados do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="50080-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="50080-118">No servidor, o RDP usa seu próprio teclado e driver de mouse para receber esses eventos de teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="50080-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="50080-119">Em uma sessão de Área de Trabalho Remota, todas as variáveis de ambiente — por exemplo, variáveis que determinam a profundidade de cor e a habilitação e a desabilitação de papel de parede — são determinadas pelas configurações de conexão de RCP-Tcp.</span><span class="sxs-lookup"><span data-stu-id="50080-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="50080-120">Isso se aplica a todas as funções e métodos que definem variáveis de ambiente na [referência de conexão Web de área de trabalho remota](remote-desktop-web-connection-reference.md) e na interface de [provedor do serviços de área de trabalho remota WMI](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="50080-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="50080-121">Recursos</span><span class="sxs-lookup"><span data-stu-id="50080-121">Features</span></span>

<span data-ttu-id="50080-122">O Microsoft RDP inclui os seguintes recursos e funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="50080-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="50080-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encripta</span><span class="sxs-lookup"><span data-stu-id="50080-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="50080-124">O RDP usa a codificação RC4 da segurança RSA, uma codificação de fluxo projetada para criptografar com eficiência pequenas quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="50080-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="50080-125">O RC4 foi projetado para comunicações seguras em redes.</span><span class="sxs-lookup"><span data-stu-id="50080-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="50080-126">Os administradores podem optar por criptografar dados usando uma chave de 56 ou 128 bits.</span><span class="sxs-lookup"><span data-stu-id="50080-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="50080-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Recursos de redução de largura de banda</span><span class="sxs-lookup"><span data-stu-id="50080-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="50080-128">O RDP dá suporte a vários mecanismos para reduzir a quantidade de dados transmitidos em uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="50080-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="50080-129">Os mecanismos incluem compactação de dados, cache persistente de bitmaps e cache de glifos e fragmentos na RAM.</span><span class="sxs-lookup"><span data-stu-id="50080-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="50080-130">O cache de bitmap persistente pode fornecer uma melhoria significativa no desempenho em relação a conexões de largura de banda baixa, especialmente ao executar aplicativos que fazem uso extensivo de bitmaps grandes.</span><span class="sxs-lookup"><span data-stu-id="50080-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="50080-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Desconexão de roaming</span><span class="sxs-lookup"><span data-stu-id="50080-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="50080-132">Um usuário pode se desconectar manualmente de uma sessão de área de trabalho remota sem fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="50080-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="50080-133">O usuário é automaticamente reconectado à sessão desconectada quando ele faz logon no sistema, seja do mesmo dispositivo ou de um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="50080-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="50080-134">Quando a sessão de um usuário é encerrada inesperadamente por uma falha de rede ou cliente, o usuário é desconectado, mas não é desconectado.</span><span class="sxs-lookup"><span data-stu-id="50080-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="50080-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mapeamento da área de transferência</span><span class="sxs-lookup"><span data-stu-id="50080-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="50080-136">Os usuários podem excluir, copiar e colar texto e gráficos entre aplicativos em execução no computador local e aqueles em execução em uma sessão de área de trabalho remota e entre sessões.</span><span class="sxs-lookup"><span data-stu-id="50080-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="50080-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirecionamento de impressão</span><span class="sxs-lookup"><span data-stu-id="50080-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="50080-138">Os aplicativos executados em uma sessão de área de trabalho remota podem ser impressos em uma impressora anexada ao dispositivo cliente.</span><span class="sxs-lookup"><span data-stu-id="50080-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="50080-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canais virtuais</span><span class="sxs-lookup"><span data-stu-id="50080-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="50080-140">Usando a arquitetura de canal virtual de RDP, os aplicativos existentes podem ser aumentados e novos aplicativos podem ser desenvolvidos para adicionar recursos que exigem comunicações entre o dispositivo cliente e um aplicativo em execução em uma sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="50080-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="50080-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Controle remoto</span><span class="sxs-lookup"><span data-stu-id="50080-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="50080-142">A equipe de suporte do computador pode exibir e controlar uma sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="50080-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="50080-143">O compartilhamento de entrada e exibição de gráficos entre duas sessões de área de trabalho remota oferece a uma pessoa de suporte a capacidade de diagnosticar e resolver problemas remotamente.</span><span class="sxs-lookup"><span data-stu-id="50080-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="50080-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Balanceamento de carga de rede</span><span class="sxs-lookup"><span data-stu-id="50080-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="50080-145">O RDP aproveita o NLB (balanceamento de carga de rede), quando disponível.</span><span class="sxs-lookup"><span data-stu-id="50080-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="50080-146">Além disso, o RDP contém os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="50080-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="50080-147">Suporte para cor de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="50080-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="50080-148">Desempenho aprimorado em conexões dial-up de baixa velocidade por meio de largura de banda reduzida.</span><span class="sxs-lookup"><span data-stu-id="50080-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="50080-149">Autenticação de cartão inteligente por meio de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="50080-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="50080-150">Gancho de teclado.</span><span class="sxs-lookup"><span data-stu-id="50080-150">Keyboard hooking.</span></span> <span data-ttu-id="50080-151">A capacidade de direcionar combinações especiais de tecla do Windows, no modo de tela inteira, para o computador local ou para um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="50080-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="50080-152">Som, unidade, porta e redirecionamento de impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="50080-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="50080-153">Sons que ocorrem no computador remoto podem ser ouvidos no computador cliente que executa o cliente RDC, e as unidades de cliente locais ficarão visíveis para a sessão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="50080-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 