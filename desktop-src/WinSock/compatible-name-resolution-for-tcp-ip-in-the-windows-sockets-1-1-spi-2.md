---
description: O Windows Sockets 1,1 definiu várias rotinas que foram usadas para a resolução de nomes IPv4 com redes TCP/IP. Essas são normalmente chamadas de funções GetXbyY e incluem o seguinte.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Resolução de nomes compatível com TCP/IP no SPI do Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781147"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="af3d2-104">Resolução de nomes compatível com TCP/IP no SPI do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="af3d2-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="af3d2-105">O Windows Sockets 1,1 definiu várias rotinas que foram usadas para a resolução de nomes IPv4 com redes TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="af3d2-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="af3d2-106">Essas são normalmente chamadas de funções **GetXbyY** e incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="af3d2-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="af3d2-107">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="af3d2-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="af3d2-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="af3d2-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="af3d2-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="af3d2-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="af3d2-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="af3d2-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="af3d2-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="af3d2-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="af3d2-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="af3d2-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="af3d2-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="af3d2-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="af3d2-114">As versões assíncronas dessas funções também foram definidas.</span><span class="sxs-lookup"><span data-stu-id="af3d2-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="af3d2-115">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="af3d2-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="af3d2-116">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="af3d2-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="af3d2-117">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="af3d2-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="af3d2-118">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="af3d2-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="af3d2-119">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="af3d2-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="af3d2-120">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="af3d2-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="af3d2-121">Essas funções são específicas para redes TCP/IP; os desenvolvedores de aplicativos independentes de protocolo não são incentivados de continuar a utilizar essas funções específicas de transporte.</span><span class="sxs-lookup"><span data-stu-id="af3d2-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="af3d2-122">No entanto, para manter a compatibilidade com versões anteriores estritas com o Windows Sockets 1,1, as funções anteriores continuam com suporte desde que pelo menos um provedor de namespace esteja presente e ofereça suporte à \_ família de endereços inet da série AF.</span><span class="sxs-lookup"><span data-stu-id="af3d2-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="af3d2-123">O *Ws2 \_32.dll* implementa essas funções de compatibilidade em termos dos novos recursos de resolução de nome independentes de protocolo usando uma sequência apropriada de chamadas de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .</span><span class="sxs-lookup"><span data-stu-id="af3d2-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="af3d2-124">Os detalhes de como as funções **GetXbyY** são mapeadas para as funções de resolução de nomes são fornecidos abaixo.</span><span class="sxs-lookup"><span data-stu-id="af3d2-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="af3d2-125">O ws2 \_32.dll lida com as diferenças entre as versões assíncronas e síncronas das funções **GetXbyY** , para que apenas a implementação das funções **GetXbyY** síncronas seja discutida.</span><span class="sxs-lookup"><span data-stu-id="af3d2-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
