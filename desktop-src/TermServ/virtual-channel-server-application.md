---
title: Aplicativo de servidor do virtual Channel
description: O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636206"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="2c250-104">Aplicativo de servidor do virtual Channel</span><span class="sxs-lookup"><span data-stu-id="2c250-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="2c250-105">O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="2c250-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="2c250-106">Observe que você deve fornecer um método para iniciar o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="2c250-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="2c250-107">Você pode fazer isso de várias maneiras; por exemplo, você pode usar um script de logon ou um programa ou script na pasta Startup.</span><span class="sxs-lookup"><span data-stu-id="2c250-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="2c250-108">Os usuários também podem iniciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c250-108">Users could also launch the application.</span></span>

<span data-ttu-id="2c250-109">Você deve armazenar o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="2c250-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="2c250-110">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **Terminal Server** \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="2c250-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="2c250-111">Para obter mais informações sobre a subchave, consulte [monitorando conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="2c250-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="2c250-112">O aplicativo de servidor pode chamar a função [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir um identificador para um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="2c250-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="2c250-113">O aplicativo pode usar o identificador em qualquer uma das funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c250-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="2c250-114">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="2c250-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="2c250-115">Fecha um identificador de canal virtual aberto.</span><span class="sxs-lookup"><span data-stu-id="2c250-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="2c250-116">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="2c250-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="2c250-117">Exclui todos os dados de entrada na fila enviados do cliente para o servidor em um canal virtual específico.</span><span class="sxs-lookup"><span data-stu-id="2c250-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="2c250-118">Essa função não é usada atualmente por Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="2c250-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="2c250-119">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="2c250-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="2c250-120">Exclui todos os dados de saída na fila enviados do servidor para o cliente em um canal virtual específico.</span><span class="sxs-lookup"><span data-stu-id="2c250-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="2c250-121">Essa função não é usada atualmente por Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="2c250-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="2c250-122">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="2c250-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="2c250-123">Retorna informações sobre um canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="2c250-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="2c250-124">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="2c250-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="2c250-125">Lê dados da extremidade do servidor de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="2c250-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="2c250-126">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="2c250-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="2c250-127">Grava dados na extremidade do servidor de um canal virtual.</span><span class="sxs-lookup"><span data-stu-id="2c250-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




