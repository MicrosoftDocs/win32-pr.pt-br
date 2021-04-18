---
description: Função gethostbyname no SPI do Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Função gethostbyname no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793904"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="24780-103">Função gethostbyname no SPI</span><span class="sxs-lookup"><span data-stu-id="24780-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="24780-104">A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ inet \_ HOSTADDRBYNAME como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="24780-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="24780-105">O nome do host é fornecido em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="24780-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="24780-106">O *\_32.dllWs2* especifica Lup \_ blob de retorno \_ e o NSP coloca uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima).</span><span class="sxs-lookup"><span data-stu-id="24780-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="24780-107">NSPs também deve respeitar esses outros \_ \_ \* sinalizadores de retorno de Lup.</span><span class="sxs-lookup"><span data-stu-id="24780-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="24780-108">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="24780-108">Flag</span></span>              | <span data-ttu-id="24780-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="24780-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24780-110">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="24780-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="24780-111">Retorna o membro do **\_ nome h** da estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="24780-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="24780-112">\_endereço de retorno de Lup \_</span><span class="sxs-lookup"><span data-stu-id="24780-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="24780-113">Retorna informações de endereçamento de [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) em estruturas de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , as informações de porta são padronizadas como zero.</span><span class="sxs-lookup"><span data-stu-id="24780-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="24780-114">Observe que essa rotina não resolve nomes de host que consistem em uma cadeia de caracteres de endereço IPv4 de decimal pontilhado.</span><span class="sxs-lookup"><span data-stu-id="24780-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
