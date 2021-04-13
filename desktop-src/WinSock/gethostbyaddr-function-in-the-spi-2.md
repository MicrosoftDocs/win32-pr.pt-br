---
description: A consulta WSALookupServiceBegin usa SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Função GetHostbyaddr no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501695"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="2468e-103">Função GetHostbyaddr no SPI</span><span class="sxs-lookup"><span data-stu-id="2468e-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="2468e-104">A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTNAMEBYADDR como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="2468e-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="2468e-105">O endereço do host é fornecido em *lpszServiceInstanceName* como uma cadeia de caracteres de endereço IPv4 com pontos decimais (por exemplo, 192.9.200.120).</span><span class="sxs-lookup"><span data-stu-id="2468e-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="2468e-106">O *\_32.dllWs2* especifica Lup \_ blob de retorno \_ e o NSP coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima).</span><span class="sxs-lookup"><span data-stu-id="2468e-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="2468e-107">NSPs também deve respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.</span><span class="sxs-lookup"><span data-stu-id="2468e-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="2468e-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="2468e-108">Flag</span></span>              | <span data-ttu-id="2468e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2468e-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2468e-110">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="2468e-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="2468e-111">Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="2468e-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="2468e-112">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="2468e-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="2468e-113">Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero.</span><span class="sxs-lookup"><span data-stu-id="2468e-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
