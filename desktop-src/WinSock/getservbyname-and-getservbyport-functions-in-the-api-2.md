---
description: As funções getservbyname e getservbyport usam a função WSALookupServiceBegin para consultar SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funções getservbyname e getservbyport na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771432"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="59b11-103">Funções getservbyname e getservbyport na API</span><span class="sxs-lookup"><span data-stu-id="59b11-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="59b11-104">As funções [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usam a função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para consultar SVCID \_ inet \_ SERVICEBYNAME como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="59b11-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="59b11-105">O membro *lpszServiceInstanceName* na estrutura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passado para a função **WSALookupServiceBegin** faz referência a uma cadeia de caracteres para indicar o nome do serviço ou a porta de serviço e (opcionalmente) o protocolo de serviço.</span><span class="sxs-lookup"><span data-stu-id="59b11-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="59b11-106">A formatação da cadeia de caracteres é ilustrada como FTP ou TCP ou 21/TCP ou apenas FTP.</span><span class="sxs-lookup"><span data-stu-id="59b11-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="59b11-107">A cadeia de caracteres não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="59b11-107">The string is not case sensitive.</span></span> <span data-ttu-id="59b11-108">A barra, se presente, separa o identificador de protocolo da parte anterior da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="59b11-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="59b11-109">O \_32.dll Ws2 especificará Lup \_ blob de retorno \_ e o provedor de namespace irá posicionar uma estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) no BLOB (usando deslocamentos em vez de ponteiros, conforme descrito acima).</span><span class="sxs-lookup"><span data-stu-id="59b11-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="59b11-110">Provedores de namespace também devem respeitar esses \_ outros \_ \* sinalizadores de retorno de Lup.</span><span class="sxs-lookup"><span data-stu-id="59b11-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="59b11-111">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="59b11-111">Flag</span></span>              | <span data-ttu-id="59b11-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="59b11-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b11-113">LUP \_ nome de retorno \_</span><span class="sxs-lookup"><span data-stu-id="59b11-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="59b11-114">Retorna o membro do **\_ nome de s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) em *lpszServiceInstanceName*.</span><span class="sxs-lookup"><span data-stu-id="59b11-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="59b11-115">\_tipo de retorno Lup \_</span><span class="sxs-lookup"><span data-stu-id="59b11-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="59b11-116">Retorna o GUID canônico em *lpServiceClassId* é entendido que um serviço identificado como FTP ou 21 pode estar em outra porta de acordo com as convenções estabelecidas localmente.</span><span class="sxs-lookup"><span data-stu-id="59b11-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="59b11-117">O parâmetro da **\_ porta s** da estrutura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicar onde o serviço pode ser contatado no ambiente local.</span><span class="sxs-lookup"><span data-stu-id="59b11-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="59b11-118">O GUID canônico retornado quando o \_ tipo de retorno Lup \_ está definido deve ser um dos GUIDs predefinidos de SVCS. h que corresponde ao número da porta indicado na estrutura **SERVENT** .</span><span class="sxs-lookup"><span data-stu-id="59b11-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="59b11-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59b11-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59b11-120">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="59b11-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="59b11-121">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="59b11-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="59b11-122">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="59b11-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



