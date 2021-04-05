---
description: Executando o código de exemplo de cliente TCP/IP completo e aplicativo de servidor.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Executando o cliente Winsock e o exemplo de código do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920910"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="5174f-103">Executando o cliente Winsock e o exemplo de código do servidor</span><span class="sxs-lookup"><span data-stu-id="5174f-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="5174f-104">Esta seção contém o código-fonte completo para os aplicativos de cliente e servidor TCP/IP:</span><span class="sxs-lookup"><span data-stu-id="5174f-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="5174f-105">Código completo do cliente Winsock</span><span class="sxs-lookup"><span data-stu-id="5174f-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="5174f-106">Código completo do servidor Winsock</span><span class="sxs-lookup"><span data-stu-id="5174f-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="5174f-107">O aplicativo de servidor deve ser iniciado antes do aplicativo cliente ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="5174f-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="5174f-108">Para executar o servidor, compile o código-fonte completo do servidor e execute o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="5174f-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="5174f-109">O aplicativo de servidor escuta na porta TCP 27015 para que um cliente se conecte.</span><span class="sxs-lookup"><span data-stu-id="5174f-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="5174f-110">Quando um cliente se conecta, o servidor recebe dados do cliente e ecoa (envia) os dados recebidos de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="5174f-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="5174f-111">Quando o cliente desliga a conexão, o servidor desliga o soquete do cliente, fecha o soquete e sai.</span><span class="sxs-lookup"><span data-stu-id="5174f-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="5174f-112">Para executar o cliente, compile o código-fonte completo do cliente e execute o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="5174f-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="5174f-113">O aplicativo cliente requer que o nome do computador ou endereço IP do computador em que o aplicativo do servidor está sendo executado seja passado como um parâmetro de linha de comando quando o cliente é executado.</span><span class="sxs-lookup"><span data-stu-id="5174f-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="5174f-114">Se o cliente e o servidor forem executados no computador de exemplo, o cliente poderá ser iniciado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5174f-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="5174f-115">**localhost do cliente**</span><span class="sxs-lookup"><span data-stu-id="5174f-115">**client localhost**</span></span>

<span data-ttu-id="5174f-116">O cliente tenta se conectar ao servidor na porta TCP 27015.</span><span class="sxs-lookup"><span data-stu-id="5174f-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="5174f-117">Depois que o cliente se conecta, o cliente envia dados ao servidor e recebe todos os dados enviados do servidor.</span><span class="sxs-lookup"><span data-stu-id="5174f-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="5174f-118">O cliente fecha o soquete e sai.</span><span class="sxs-lookup"><span data-stu-id="5174f-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5174f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5174f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5174f-120">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="5174f-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



