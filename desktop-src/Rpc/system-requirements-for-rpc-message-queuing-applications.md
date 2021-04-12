---
title: Requisitos do sistema para aplicativos de enfileiramento RPC-Message
description: Para usar o transporte de enfileiramento de mensagens em um aplicativo cliente/servidor RPC, o servidor e os computadores cliente devem ter a plataforma de sistema operacional e o software de enfileiramento de mensagens apropriados instalados.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366527"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="18352-103">Requisitos do sistema para aplicativos de enfileiramento RPC-Message</span><span class="sxs-lookup"><span data-stu-id="18352-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="18352-104">Para usar o transporte de enfileiramento de mensagens em um aplicativo cliente/servidor RPC, o servidor e os computadores cliente devem ter a plataforma de sistema operacional e o software de enfileiramento de mensagens apropriados instalados.</span><span class="sxs-lookup"><span data-stu-id="18352-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="18352-105">Os requisitos para computadores servidores são:</span><span class="sxs-lookup"><span data-stu-id="18352-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="18352-106">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="18352-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="18352-107">SQL Server versão 6,5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="18352-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="18352-108">Controlador corporativo primário do enfileiramento de mensagens ou controlador de site primário.</span><span class="sxs-lookup"><span data-stu-id="18352-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="18352-109">DLL de transporte do lado do servidor RPC (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="18352-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="18352-110">Os requisitos para computadores cliente são:</span><span class="sxs-lookup"><span data-stu-id="18352-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="18352-111">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="18352-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="18352-112">Cliente de enfileiramento de mensagens da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="18352-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="18352-113">DLL de transporte do lado do cliente RPC (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="18352-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="18352-114">Quando os componentes do MSMQ são instalados nos computadores cliente e servidor, os registros do sistema são configurados automaticamente para incluir o protocolo de transporte de enfileiramento de mensagens do [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="18352-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="18352-115">Para criar seu aplicativo RPC-MSMQ, você precisará do seguinte:</span><span class="sxs-lookup"><span data-stu-id="18352-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="18352-116">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou posterior</span><span class="sxs-lookup"><span data-stu-id="18352-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="18352-117">MIDL versão 3.1.76 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="18352-117">MIDL version 3.1.76 or later.</span></span>

 

 