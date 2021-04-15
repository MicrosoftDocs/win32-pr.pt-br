---
description: Todos os processos (aplicativos ou DLLs) que chamam funções Winsock devem inicializar o uso da DLL do Windows Sockets antes de fazer outras chamadas de funções do Winsock. Isso também faz com que o Winsock tenha suporte no sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inicializando o Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501691"
---
# <a name="initializing-winsock"></a><span data-ttu-id="b456b-104">Inicializando o Winsock</span><span class="sxs-lookup"><span data-stu-id="b456b-104">Initializing Winsock</span></span>

<span data-ttu-id="b456b-105">Todos os processos (aplicativos ou DLLs) que chamam funções Winsock devem inicializar o uso da DLL do Windows Sockets antes de fazer outras chamadas de funções do Winsock.</span><span class="sxs-lookup"><span data-stu-id="b456b-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="b456b-106">Isso também faz com que o Winsock tenha suporte no sistema.</span><span class="sxs-lookup"><span data-stu-id="b456b-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="b456b-107">**Para inicializar o Winsock**</span><span class="sxs-lookup"><span data-stu-id="b456b-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="b456b-108">Crie um objeto [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) chamado WSADATA.</span><span class="sxs-lookup"><span data-stu-id="b456b-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="b456b-109">Chame [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) e retorne seu valor como um inteiro e verifique se há erros.</span><span class="sxs-lookup"><span data-stu-id="b456b-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="b456b-110">A função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) é chamada para iniciar o uso de ws2 \_32.dll.</span><span class="sxs-lookup"><span data-stu-id="b456b-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="b456b-111">A estrutura [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contém informações sobre a implementação do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="b456b-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="b456b-112">O parâmetro MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) faz uma solicitação para a versão 2,2 do Winsock no sistema e define a versão passada como a versão mais recente do suporte do Windows Sockets que o chamador pode usar.</span><span class="sxs-lookup"><span data-stu-id="b456b-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="b456b-113">Próxima etapa para um cliente: [criando um soquete para o cliente](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="b456b-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="b456b-114">Próxima etapa para um servidor: [criando um soquete para o servidor](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="b456b-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b456b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b456b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b456b-116">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="b456b-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="b456b-117">Criando um aplicativo Winsock básico</span><span class="sxs-lookup"><span data-stu-id="b456b-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



