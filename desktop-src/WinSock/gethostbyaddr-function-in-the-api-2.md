---
description: A função GetHostbyaddr usa a função WSALookupServiceBegin para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Função GetHostbyaddr na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791630"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="6e8be-103">Função GetHostbyaddr na API</span><span class="sxs-lookup"><span data-stu-id="6e8be-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="6e8be-104">A função [**GetHostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa a função [**WSALOOKUPSERVICEBEGIN**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="6e8be-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="6e8be-105">O endereço do host é fornecido como uma cadeia de caracteres IPv4 decimnal pontilhada (por exemplo, "192.9.200.120") no membro *lpszServiceInstanceName* da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passada para a função **WSALookupServiceBegin** .</span><span class="sxs-lookup"><span data-stu-id="6e8be-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="6e8be-106">O \_32.dll Ws2 especifica Lup \_ blob de retorno \_ e o provedor de serviço de nome coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima).</span><span class="sxs-lookup"><span data-stu-id="6e8be-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="6e8be-107">Provedores de serviço de nome também devem respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.</span><span class="sxs-lookup"><span data-stu-id="6e8be-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="6e8be-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="6e8be-108">Flag</span></span>              | <span data-ttu-id="6e8be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e8be-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8be-110">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="6e8be-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="6e8be-111">Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="6e8be-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="6e8be-112">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="6e8be-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="6e8be-113">Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero.</span><span class="sxs-lookup"><span data-stu-id="6e8be-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e8be-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e8be-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e8be-115">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="6e8be-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="6e8be-116">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="6e8be-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="6e8be-117">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="6e8be-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
