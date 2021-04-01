---
description: Um pipe nomeado é um pipe nomeado, unidirecional ou bidirecional para comunicação entre o servidor de pipe e um ou mais clientes de pipe.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Pipes nomeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921869"
---
# <a name="named-pipes"></a><span data-ttu-id="2243e-103">Pipes nomeados</span><span class="sxs-lookup"><span data-stu-id="2243e-103">Named Pipes</span></span>

<span data-ttu-id="2243e-104">Um *pipe nomeado* é um pipe nomeado, unidirecional ou bidirecional para comunicação entre o servidor de pipe e um ou mais clientes de pipe.</span><span class="sxs-lookup"><span data-stu-id="2243e-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="2243e-105">Todas as instâncias de um pipe nomeado compartilham o mesmo nome de pipe, mas cada instância tem seus próprios buffers e identificadores e fornece um canal separado para comunicação de cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="2243e-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="2243e-106">O uso de instâncias permite que vários clientes de pipe usem o mesmo pipe nomeado simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2243e-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="2243e-107">Qualquer processo pode acessar pipes nomeados, sujeito a verificações de segurança, tornando os pipes nomeados uma forma fácil de comunicação entre processos relacionados ou não relacionados.</span><span class="sxs-lookup"><span data-stu-id="2243e-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="2243e-108">Qualquer processo pode atuar como um servidor e um cliente, tornando possível a comunicação ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="2243e-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="2243e-109">Conforme usado aqui, o servidor de pipe de termo se refere a um processo que cria um pipe nomeado e o cliente de pipe de termo refere-se a um processo que se conecta a uma instância de um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="2243e-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="2243e-110">A função do lado do servidor para instanciar um pipe nomeado é [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span><span class="sxs-lookup"><span data-stu-id="2243e-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="2243e-111">A função do lado do servidor para aceitar uma conexão é [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="2243e-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="2243e-112">Um processo de cliente se conecta a um pipe nomeado usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="2243e-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="2243e-113">Pipes nomeados podem ser usados para fornecer comunicação entre processos no mesmo computador ou entre processos em computadores diferentes em uma rede.</span><span class="sxs-lookup"><span data-stu-id="2243e-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="2243e-114">Se o serviço do servidor estiver em execução, todos os pipes nomeados poderão ser acessados remotamente.</span><span class="sxs-lookup"><span data-stu-id="2243e-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="2243e-115">Se você pretende usar apenas um pipe nomeado localmente, negue o acesso à rede de Autoridade NT \\ ou alterne para o RPC local.</span><span class="sxs-lookup"><span data-stu-id="2243e-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="2243e-116">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="2243e-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2243e-117">Nomes de pipe</span><span class="sxs-lookup"><span data-stu-id="2243e-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="2243e-118">Modos abertos do pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2243e-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="2243e-119">Modos de tipo de pipe nomeado, leitura e espera</span><span class="sxs-lookup"><span data-stu-id="2243e-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="2243e-120">Instâncias de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2243e-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="2243e-121">Operações de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2243e-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="2243e-122">Entrada e saída síncronas e sobrepostas</span><span class="sxs-lookup"><span data-stu-id="2243e-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="2243e-123">Segurança de pipe nomeado e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="2243e-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="2243e-124">Representando um cliente de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="2243e-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="2243e-125">Usando pipes</span><span class="sxs-lookup"><span data-stu-id="2243e-125">Using Pipes</span></span>](using-pipes.md)

 

 
