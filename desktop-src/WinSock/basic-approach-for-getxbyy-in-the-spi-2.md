---
description: A maioria das funções GetXbyY são convertidas por Ws2 \_32.dll em uma sequência WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa um conjunto de GUIDs especiais como a classe de serviço.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Abordagem básica para GetXbyY no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827123"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="3e49e-103">Abordagem básica para GetXbyY no SPI</span><span class="sxs-lookup"><span data-stu-id="3e49e-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="3e49e-104">A maioria das funções **GetXbyY** são convertidas por Ws2 \_32.dll em uma sequência [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa um conjunto de GUIDs especiais como a classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="3e49e-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="3e49e-105">Essas GUIDs identificam o tipo de operação **GetXbyY** que está sendo emulada.</span><span class="sxs-lookup"><span data-stu-id="3e49e-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="3e49e-106">A consulta é restrita a essas NSPs que dão suporte ao inet da AF \_ .</span><span class="sxs-lookup"><span data-stu-id="3e49e-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="3e49e-107">Sempre que uma função **GetXbyY** retorna uma estrutura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) ou [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , o ws2 \_32.dll especificará o \_ sinalizador de retorno de blob Lup \_ em **WSALookupServiceBegin** para que as informações desejadas sejam retornadas pelo NSP.</span><span class="sxs-lookup"><span data-stu-id="3e49e-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="3e49e-108">Essas estruturas devem ser ligeiramente modificadas, pois os ponteiros contidos em devem ser substituídos por deslocamentos que são relativos ao início dos dados do blob.</span><span class="sxs-lookup"><span data-stu-id="3e49e-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="3e49e-109">É claro que todos os valores referenciados por esses membros de ponteiro devem estar completamente contidos no BLOB, e todas as cadeias de caracteres são ASCII.</span><span class="sxs-lookup"><span data-stu-id="3e49e-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



