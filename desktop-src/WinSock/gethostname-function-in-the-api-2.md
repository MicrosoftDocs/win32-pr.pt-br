---
description: A função GetHostName usa a função WSALookupServiceBegin para consultar o \_ nome de host SVCID como o GUID de classe de serviço.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Função GetHostName na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787745"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="45c8e-103">Função GetHostName na API</span><span class="sxs-lookup"><span data-stu-id="45c8e-103">gethostname Function in the API</span></span>

<span data-ttu-id="45c8e-104">A função [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar o \_ nome de host SVCID como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="45c8e-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="45c8e-105">Se o membro **lpszServiceInstanceName** da estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a função **WSALookupServiceBegin** for **nulo** ou fizer referência a uma cadeia de caracteres **nula** (ou seja.</span><span class="sxs-lookup"><span data-stu-id="45c8e-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="45c8e-106">""), o host local deve ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="45c8e-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="45c8e-107">Caso contrário, ocorrerá uma pesquisa em um nome de host especificado.</span><span class="sxs-lookup"><span data-stu-id="45c8e-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="45c8e-108">Para fins de emulação de **GetHostName** , o \_32.dll Ws2 especifica um ponteiro **nulo** para o membro **lpszServiceInstanceName** e especifica Lup \_ nome de retorno \_ para que o nome do host seja retornado no membro **lpszServiceInstanceName** .</span><span class="sxs-lookup"><span data-stu-id="45c8e-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="45c8e-109">Se um aplicativo usar essa consulta e especificar \_ \_ o endereço de retorno de Lup, então ele será fornecido em uma estrutura de [**\_ informações de CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="45c8e-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="45c8e-110">A \_ ação de blob de retorno Lup \_ é indefinida para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="45c8e-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="45c8e-111">As informações de porta são padronizadas para zero, a menos que o membro **lpszQueryString** da estrutura **WSAQUERYSET** passada para a função **WSALOOKUPSERVICEBEGIN** referencie um serviço como FTP. nesse caso, o endereço de transporte completo do serviço indicado é fornecido.</span><span class="sxs-lookup"><span data-stu-id="45c8e-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45c8e-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45c8e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45c8e-113">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="45c8e-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="45c8e-114">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="45c8e-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="45c8e-115">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="45c8e-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
