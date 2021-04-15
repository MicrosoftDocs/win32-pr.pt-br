---
description: A maioria das funções getXbyY são convertidas pelo \_32.dll Ws2 para uma sequência WSALookupServiceBegin, WSALookupServiceNext e WSALookupServiceEnd que usa um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Abordagem básica para GetXbyY na API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501707"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="ea7e2-103">Abordagem básica para GetXbyY na API</span><span class="sxs-lookup"><span data-stu-id="ea7e2-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="ea7e2-104">A maioria das funções **getXbyY** são convertidas pelo \_32.dll Ws2 para uma sequência [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um conjunto de GUIDs especiais como a classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="ea7e2-105">Essas GUIDs identificam o tipo de operação **getXbyY** que está sendo emulada.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="ea7e2-106">A consulta é restrita a esses provedores de serviços de nomes que dão suporte ao inet da AF \_ .</span><span class="sxs-lookup"><span data-stu-id="ea7e2-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="ea7e2-107">Sempre que uma função **getXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , o ws2 \_32.dll especifica o \_ sinalizador de retorno de blob Lup \_ em **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo provedor de serviços de nome.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="ea7e2-108">Essas estruturas devem ser ligeiramente modificadas, pois os ponteiros contidos em devem ser substituídos por deslocamentos que são relativos ao início dos dados do blob.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="ea7e2-109">É claro que todos os valores referenciados por esses parâmetros de ponteiro devem estar completamente contidos no BLOB, e todas as cadeias de caracteres são ASCII.</span><span class="sxs-lookup"><span data-stu-id="ea7e2-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea7e2-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea7e2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea7e2-111">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="ea7e2-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="ea7e2-112">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="ea7e2-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="ea7e2-113">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="ea7e2-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



