---
description: Função gethostbyname na API do Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Função gethostbyname na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090392"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="f76e7-103">Função gethostbyname na API</span><span class="sxs-lookup"><span data-stu-id="f76e7-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="f76e7-104">A função [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa a função [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTADDRBYNAME como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="f76e7-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="f76e7-105">O nome do host é fornecido no membro **lpszServiceInstanceName** na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passada para a função **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="f76e7-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="f76e7-106">O \_32.dll Ws2 especifica Lup \_ blob de retorno \_ e o provedor de serviço de nome coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima).</span><span class="sxs-lookup"><span data-stu-id="f76e7-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="f76e7-107">Provedores de serviço de nome também devem respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.</span><span class="sxs-lookup"><span data-stu-id="f76e7-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="f76e7-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="f76e7-108">Flag</span></span>              | <span data-ttu-id="f76e7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f76e7-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f76e7-110">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="f76e7-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="f76e7-111">Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="f76e7-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="f76e7-112">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="f76e7-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="f76e7-113">Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero.</span><span class="sxs-lookup"><span data-stu-id="f76e7-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="f76e7-114">Observe que essa rotina não resolve nomes de host que consistem em um endereço IPv4 pontilhado.</span><span class="sxs-lookup"><span data-stu-id="f76e7-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f76e7-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f76e7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f76e7-116">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="f76e7-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="f76e7-117">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="f76e7-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="f76e7-118">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="f76e7-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
