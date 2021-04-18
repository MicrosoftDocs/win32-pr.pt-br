---
title: Desenvolvimento de cliente usando identificadores de contexto
description: O único uso de um programa cliente para um identificador de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498775"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="56cee-103">Desenvolvimento de cliente usando identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="56cee-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="56cee-104">O único uso de um programa cliente para um identificador de contexto é passá-lo para o servidor sempre que o cliente fizer uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="56cee-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="56cee-105">O aplicativo cliente não precisa acessar o conteúdo do identificador.</span><span class="sxs-lookup"><span data-stu-id="56cee-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="56cee-106">Ele não deve tentar alterar os dados de identificador de contexto de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="56cee-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="56cee-107">Os procedimentos remotos que o cliente invoca executam todas as operações necessárias no contexto do servidor.</span><span class="sxs-lookup"><span data-stu-id="56cee-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="56cee-108">Antes de solicitar um identificador de contexto de um servidor, os clientes devem estabelecer uma ligação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="56cee-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="56cee-109">O cliente pode usar um identificador de associação automático, implícito ou explícito.</span><span class="sxs-lookup"><span data-stu-id="56cee-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="56cee-110">Com um identificador de associação válido, o cliente pode chamar um procedimento remoto no servidor que retorna um identificador de contexto aberto (não **nulo**) ou passa um por um parâmetro de **\[ saída \]** na lista de parâmetros do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="56cee-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="56cee-111">Os clientes podem usar identificadores de contexto abertos de qualquer maneira que exijam.</span><span class="sxs-lookup"><span data-stu-id="56cee-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="56cee-112">No entanto, eles devem invalidar o identificador quando eles não precisarem mais dele.</span><span class="sxs-lookup"><span data-stu-id="56cee-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="56cee-113">Há duas maneiras de fazer isso:</span><span class="sxs-lookup"><span data-stu-id="56cee-113">There are two way to do this:</span></span>

-   <span data-ttu-id="56cee-114">Para invocar um procedimento remoto oferecido pelo programa de servidor que libera o contexto e fecha o identificador de contexto (define-o como **nulo**).</span><span class="sxs-lookup"><span data-stu-id="56cee-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="56cee-115">Quando o servidor estiver inacessível, chame a função [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="56cee-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="56cee-116">A segunda abordagem limpa apenas o estado do lado do cliente e não limpa o estado do lado do servidor, portanto, ele deve ser usado somente quando a partição de rede for suspeita e o cliente e o servidor farão uma limpeza independente.</span><span class="sxs-lookup"><span data-stu-id="56cee-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="56cee-117">O servidor executa a limpeza independente por meio da rotina de execução, o cliente faz isso usando a função [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="56cee-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="56cee-118">O fragmento de código a seguir apresenta um exemplo de como um cliente pode usar um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="56cee-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="56cee-119">Para exibir a definição da interface que este exemplo usa, consulte [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="56cee-120">Para a implementação do servidor, consulte [desenvolvimento de servidor usando identificadores de contexto](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="56cee-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="56cee-121">Neste exemplo, o cliente chama RemoteOpen para obter um identificador de contexto que contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="56cee-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="56cee-122">O cliente pode usar o identificador de contexto em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="56cee-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="56cee-123">Como ele não precisa mais do identificador de associação, o cliente pode liberar o identificador explícito usado para criar o identificador de contexto:</span><span class="sxs-lookup"><span data-stu-id="56cee-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="56cee-124">O aplicativo cliente neste exemplo usa um procedimento chamado RemoteRead para ler um arquivo de dados no servidor até encontrar um final de arquivo.</span><span class="sxs-lookup"><span data-stu-id="56cee-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="56cee-125">Em seguida, ele fecha o arquivo chamando RemoteClose.</span><span class="sxs-lookup"><span data-stu-id="56cee-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="56cee-126">O identificador de contexto aparece como um parâmetro nas funções RemoteRead e RemoteClose como:</span><span class="sxs-lookup"><span data-stu-id="56cee-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




