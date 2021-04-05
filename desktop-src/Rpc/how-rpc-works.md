---
title: Como funciona o RPC
description: As ferramentas de RPC o tornam aparentemente para os usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636346"
---
# <a name="how-rpc-works"></a><span data-ttu-id="3221c-103">Como funciona o RPC</span><span class="sxs-lookup"><span data-stu-id="3221c-103">How RPC Works</span></span>

<span data-ttu-id="3221c-104">As ferramentas de RPC o tornam aparentemente para os usuários como se um cliente chama diretamente um procedimento localizado em um programa de servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="3221c-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="3221c-105">O cliente e o servidor têm seus próprios espaços de endereço; ou seja, cada um tem seu próprio recurso de memória alocado aos dados usados pelo procedimento.</span><span class="sxs-lookup"><span data-stu-id="3221c-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="3221c-106">A figura a seguir ilustra a arquitetura RPC.</span><span class="sxs-lookup"><span data-stu-id="3221c-106">The following figure illustrates the RPC architecture.</span></span>

![arquitetura de RPC](images/prog-a11.png)

<span data-ttu-id="3221c-108">Como mostra a ilustração, o aplicativo cliente chama um procedimento de stub local em vez do código real que implementa o procedimento.</span><span class="sxs-lookup"><span data-stu-id="3221c-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="3221c-109">Os stubs são compilados e vinculados com o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="3221c-110">Em vez de conter o código real que implementa o procedimento remoto, o código stub do cliente:</span><span class="sxs-lookup"><span data-stu-id="3221c-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="3221c-111">Recupera os parâmetros necessários do espaço de endereço do cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="3221c-112">Traduz os parâmetros conforme necessário em um formato NDR padrão para transmissão pela rede.</span><span class="sxs-lookup"><span data-stu-id="3221c-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="3221c-113">Chama funções na biblioteca de tempo de execução do cliente RPC para enviar a solicitação e seus parâmetros para o servidor.</span><span class="sxs-lookup"><span data-stu-id="3221c-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="3221c-114">O servidor executa as etapas a seguir para chamar o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3221c-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="3221c-115">As funções de biblioteca de tempo de execução RPC do servidor aceitam a solicitação e chamam o procedimento de stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="3221c-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="3221c-116">O stub do servidor recupera os parâmetros do buffer de rede e os converte do formato de transmissão de rede para o formato que o servidor precisa.</span><span class="sxs-lookup"><span data-stu-id="3221c-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="3221c-117">O stub de servidor chama o procedimento real no servidor.</span><span class="sxs-lookup"><span data-stu-id="3221c-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="3221c-118">Em seguida, o procedimento remoto é executado, possivelmente gerando parâmetros de saída e um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3221c-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="3221c-119">Quando o procedimento remoto é concluído, uma sequência semelhante de etapas retorna os dados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="3221c-120">O procedimento remoto retorna seus dados para o stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="3221c-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="3221c-121">O stub de servidor converte parâmetros de saída para o formato necessário para transmissão pela rede e os retorna para as funções de biblioteca de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="3221c-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="3221c-122">As funções de biblioteca de tempo de execução RPC do servidor transmitem os dados na rede para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="3221c-123">O cliente conclui o processo aceitando os dados pela rede e retornando-os para a função de chamada.</span><span class="sxs-lookup"><span data-stu-id="3221c-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="3221c-124">A biblioteca de tempo de execução RPC do cliente recebe os valores de retorno de procedimento remoto e os retorna ao stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="3221c-125">O stub do cliente converte os dados de seu NDR para o formato usado pelo computador cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="3221c-126">O stub grava dados na memória do cliente e retorna o resultado para o programa de chamada no cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="3221c-127">O procedimento de chamada continua como se o procedimento tivesse sido chamado no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="3221c-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="3221c-128">As bibliotecas de tempo de execução são fornecidas em duas partes: uma biblioteca de importação, que é vinculada ao aplicativo e à biblioteca de tempo de execução RPC, que é implementada como uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="3221c-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="3221c-129">O aplicativo de servidor contém chamadas para as funções de biblioteca de tempo de execução do servidor que registram a interface do servidor e permitem que o servidor aceite chamadas de procedimento remotas.</span><span class="sxs-lookup"><span data-stu-id="3221c-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="3221c-130">O aplicativo de servidor também contém os procedimentos remotos específicos do aplicativo que são chamados pelos aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="3221c-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




