---
description: Observe que todas as funções do Windows Sockets 1,1 para resolução de nomes são específicas para redes TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760975"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="f366d-103">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="f366d-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="f366d-104">Todas as funções do Windows Sockets 1,1 para resolução de nomes são específicas para redes TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="f366d-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="f366d-105">Os desenvolvedores de aplicativos são altamente desencorajados de continuar a utilizar essas funções específicas de transporte que dão suporte apenas ao IPv4.</span><span class="sxs-lookup"><span data-stu-id="f366d-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="f366d-106">Os desenvolvedores de aplicativos devem usar as seguintes funções que são independentes de protocolo e dão suporte à resolução de nomes IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="f366d-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="f366d-107">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="f366d-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="f366d-108">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="f366d-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="f366d-109">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="f366d-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="f366d-110">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="f366d-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="f366d-111">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="f366d-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="f366d-112">O Windows Sockets 1,1 definiu várias rotinas usadas para a resolução de nomes com redes TCP/IP (IP versão 4).</span><span class="sxs-lookup"><span data-stu-id="f366d-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="f366d-113">Às vezes, elas são chamadas de funções **getXbyY** e incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f366d-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="f366d-114">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="f366d-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="f366d-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="f366d-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="f366d-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="f366d-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="f366d-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="f366d-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="f366d-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="f366d-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="f366d-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="f366d-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="f366d-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="f366d-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="f366d-121">As versões assíncronas dessas funções também foram definidas.</span><span class="sxs-lookup"><span data-stu-id="f366d-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="f366d-122">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="f366d-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="f366d-123">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="f366d-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="f366d-124">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="f366d-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="f366d-125">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="f366d-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="f366d-126">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="f366d-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="f366d-127">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="f366d-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="f366d-128">Há também duas funções, agora implementadas no Winsock2.dll, usadas para converter a notação de endereço IPv4 pontilhada de uma cadeia de caracteres e representações binárias, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f366d-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="f366d-129">**\_endereço inet**</span><span class="sxs-lookup"><span data-stu-id="f366d-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="f366d-130">**\_NTOA inet**</span><span class="sxs-lookup"><span data-stu-id="f366d-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="f366d-131">Para manter a compatibilidade com versões anteriores estritas com o Windows Sockets 1,1, todas as funções somente IPv4 mais antigas continuam a ter suporte, desde que pelo menos um provedor de namespace esteja presente e ofereça suporte à \_ família de endereços inet da série AF (essas funções não são relevantes para o IP versão 6, indicadas por AF \_ INET6).</span><span class="sxs-lookup"><span data-stu-id="f366d-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="f366d-132">O \_32.dll Ws2 implementa essas funções de compatibilidade em termos dos novos recursos de resolução de nome independentes de protocolo usando uma sequência apropriada [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)de / chamadas de função **Next** / **end** de WSALookupServiceBegin.</span><span class="sxs-lookup"><span data-stu-id="f366d-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="f366d-133">Os detalhes de como as funções **getXbyY** são mapeadas para as funções de resolução de nomes são fornecidos abaixo.</span><span class="sxs-lookup"><span data-stu-id="f366d-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="f366d-134">O WSs2 \_32.dll lida com as diferenças entre as versões assíncronas e síncronas das funções **getXbyY** , de modo que apenas a implementação das funções **getXbyY** síncronas é discutida.</span><span class="sxs-lookup"><span data-stu-id="f366d-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="f366d-135">Esta seção descreve a resolução de nome compatível para TCP/IP na API do Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="f366d-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="f366d-136">A lista a seguir descreve os tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="f366d-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="f366d-137">Abordagem básica para GetXbyY na API</span><span class="sxs-lookup"><span data-stu-id="f366d-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="f366d-138">Funções getprotobyname e getprotobynumber na API</span><span class="sxs-lookup"><span data-stu-id="f366d-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="f366d-139">Funções getservbyname e getservbyport na API</span><span class="sxs-lookup"><span data-stu-id="f366d-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="f366d-140">Função gethostbyname na API</span><span class="sxs-lookup"><span data-stu-id="f366d-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="f366d-141">Função GetHostbyaddr na API</span><span class="sxs-lookup"><span data-stu-id="f366d-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="f366d-142">Função GetHostName na API</span><span class="sxs-lookup"><span data-stu-id="f366d-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="f366d-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f366d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f366d-144">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="f366d-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="f366d-145">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="f366d-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
