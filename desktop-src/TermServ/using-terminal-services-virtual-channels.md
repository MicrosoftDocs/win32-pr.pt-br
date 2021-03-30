---
title: Usando Serviços de Área de Trabalho Remota canais virtuais
description: Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635319"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="b669c-103">Usando Serviços de Área de Trabalho Remota canais virtuais</span><span class="sxs-lookup"><span data-stu-id="b669c-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="b669c-104">Para implementar um canal virtual, você fornece os módulos de cliente e servidor do aplicativo de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="b669c-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="b669c-105">O módulo de servidor pode ser um aplicativo de modo de usuário ou um driver de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="b669c-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="b669c-106">O módulo do cliente deve ser uma DLL.</span><span class="sxs-lookup"><span data-stu-id="b669c-106">The client module must be a DLL.</span></span>

<span data-ttu-id="b669c-107">Para obter descrições desses módulos, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b669c-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b669c-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b669c-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b669c-109">Aplicativo de servidor do virtual Channel</span><span class="sxs-lookup"><span data-stu-id="b669c-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="b669c-110">O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="b669c-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="b669c-111">Observe que você deve fornecer um método para iniciar o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="b669c-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="b669c-112">DLL de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="b669c-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="b669c-113">O cliente de um aplicativo de canais virtuais é uma DLL que é carregada durante a inicialização do Serviços de Área de Trabalho Remota no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="b669c-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="b669c-114">A DLL deve ser registrada no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="b669c-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="b669c-115">Registro de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="b669c-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="b669c-116">Você deve armazenar o nome da DLL do cliente no registro.</span><span class="sxs-lookup"><span data-stu-id="b669c-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="b669c-117">Canais virtuais persistentes de controle remoto</span><span class="sxs-lookup"><span data-stu-id="b669c-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="b669c-118">Um canal virtual persistente de controle remoto não é fechado quando um controle remoto se conecta ou se desconecta da sessão conectada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b669c-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="b669c-119">Os dados continuarão a ser transmitidos e recebidos por meio desse canal.</span><span class="sxs-lookup"><span data-stu-id="b669c-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="b669c-120">Canais virtuais dinâmicos</span><span class="sxs-lookup"><span data-stu-id="b669c-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="b669c-121">As APIs de canal virtual dinâmico (DVC) estendem as APIs de canal virtual existentes para Serviços de Área de Trabalho Remota, conhecidas como APIs de SVC (canal virtual estático).</span><span class="sxs-lookup"><span data-stu-id="b669c-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="b669c-122">Se você tiver habilitado um aplicativo de canal virtual em sua implantação de Serviços de Área de Trabalho Remota, também poderá disponibilizar o aplicativo para computadores cliente que acessam o servidor Host da Sessão RD por meio do controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="b669c-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="b669c-123">Para obter mais informações, consulte [usando o controle ActiveX área de trabalho remota com canais virtuais](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="b669c-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




