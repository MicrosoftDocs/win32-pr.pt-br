---
title: Canais virtuais Serviços de Área de Trabalho Remota
description: Os canais virtuais são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo Serviços de Área de Trabalho Remota.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292114"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="cb998-103">Canais virtuais Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="cb998-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="cb998-104">Os *canais virtuais* são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="cb998-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="cb998-105">Exemplos de aprimoramentos funcionais podem incluir: suporte para tipos especiais de hardware, áudio ou outras adições à funcionalidade básica fornecida pelo Serviços de Área de Trabalho Remota [protocolo RDP](remote-desktop-protocol.md) (RDP).</span><span class="sxs-lookup"><span data-stu-id="cb998-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="cb998-106">O protocolo RDP fornece gerenciamento multiplexado de vários canais virtuais.</span><span class="sxs-lookup"><span data-stu-id="cb998-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb998-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cb998-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cb998-108">Usando Serviços de Área de Trabalho Remota canais virtuais</span><span class="sxs-lookup"><span data-stu-id="cb998-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="cb998-109">Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb998-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="cb998-110">Referência de canais virtuais dinâmicos</span><span class="sxs-lookup"><span data-stu-id="cb998-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="cb998-111">As interfaces de cliente do canal virtual dinâmico (DVC) têm suporte pelo Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="cb998-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="cb998-112">Referência de canais virtuais de gráficos</span><span class="sxs-lookup"><span data-stu-id="cb998-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="cb998-113">A referência de canais virtuais de gráficos contém elementos de programação que permitem criar um canal virtual Graphics.</span><span class="sxs-lookup"><span data-stu-id="cb998-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="cb998-114">Um aplicativo de canal virtual tem duas partes, um módulo de cliente e um módulo de servidor.</span><span class="sxs-lookup"><span data-stu-id="cb998-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="cb998-115">O módulo de servidor é um programa executável em execução no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="cb998-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="cb998-116">O módulo do cliente é uma DLL que deve ser carregada na memória no computador cliente quando o programa cliente do Conexão de Área de Trabalho Remota (RDC) é executado.</span><span class="sxs-lookup"><span data-stu-id="cb998-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="cb998-117">Os canais virtuais podem adicionar aprimoramentos funcionais a um cliente Conexão de Área de Trabalho Remota (RDC), independentemente do protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="cb998-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="cb998-118">Com o suporte ao canal virtual, novos recursos podem ser adicionados sem a necessidade de atualizar o software cliente ou servidor ou o protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="cb998-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="cb998-119">Quatro classes principais de usuários de canais virtuais foram identificadas:</span><span class="sxs-lookup"><span data-stu-id="cb998-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="cb998-120">Drivers gerais de modo kernel, como drivers de impressora ou serial.</span><span class="sxs-lookup"><span data-stu-id="cb998-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="cb998-121">Redirecionamento de sistema de arquivos (esse é apenas um caso especial de um driver de modo kernel geral).</span><span class="sxs-lookup"><span data-stu-id="cb998-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="cb998-122">Aplicativos de modo de usuário, por exemplo, recortar e colar remotamente.</span><span class="sxs-lookup"><span data-stu-id="cb998-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="cb998-123">Dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="cb998-123">Audio devices.</span></span>

<span data-ttu-id="cb998-124">Para obter mais informações, consulte [usando serviços de área de trabalho remota canais virtuais](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="cb998-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="cb998-125">Se você tiver habilitado um aplicativo de canais virtuais em sua implantação do Serviços de Área de Trabalho Remota, poderá disponibilizar o aplicativo para os computadores cliente que acessam o servidor Host da Sessão RD por meio do Área de Trabalho Remota controle ActiveX da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb998-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="cb998-126">Para obter mais informações, consulte [canais virtuais programáveis](scriptable-virtual-channels.md) e [usando o controle ActiveX área de trabalho remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="cb998-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




