---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Funções auxiliares no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793297"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="73b6d-103">Funções auxiliares no SPI</span><span class="sxs-lookup"><span data-stu-id="73b6d-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="73b6d-104">**NSPGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="73b6d-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="73b6d-105">A função [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) recupera informações de esquema de classe de serviço que foram retidas por um provedor de namespace.</span><span class="sxs-lookup"><span data-stu-id="73b6d-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="73b6d-106">Ele também é usado pela DLL do Windows Sockets 2 em sua implementação de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span><span class="sxs-lookup"><span data-stu-id="73b6d-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="73b6d-107">As macros a seguir definidas no arquivo de cabeçalho *Svcguid. h* e podem ajudar no mapeamento entre classes de serviço conhecidas e esses namespaces.</span><span class="sxs-lookup"><span data-stu-id="73b6d-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="73b6d-108">Nome da macro</span><span class="sxs-lookup"><span data-stu-id="73b6d-108">Macro name</span></span>                                                                              | <span data-ttu-id="73b6d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="73b6d-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b6d-110">**SVCID \_ TCP (porta)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="73b6d-111">**SVCID \_ UDP (porta)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="73b6d-112">Dada uma porta TCP ou UDP para o protocolo de Internet, retorna o GUID.</span><span class="sxs-lookup"><span data-stu-id="73b6d-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="73b6d-113">**é \_ SVCID \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="73b6d-114">**é \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="73b6d-115">Retornará **true** se o GUID para TCP ou UDP estiver dentro do intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="73b6d-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="73b6d-116">**PORTA \_ de \_ SVCID \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="73b6d-117">**PORTA \_ do \_ SVCID \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="73b6d-118">Retorna a porta TCP ou UDP associada ao GUID.</span><span class="sxs-lookup"><span data-stu-id="73b6d-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="73b6d-119">**SVCID \_ NetWare (SAPID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="73b6d-120">Dado o identificador do protocolo SAP, retorna o GUID.</span><span class="sxs-lookup"><span data-stu-id="73b6d-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="73b6d-121">Essa macro é usada com o namespace do SAP em um ambiente do NetWare.</span><span class="sxs-lookup"><span data-stu-id="73b6d-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="73b6d-122">**SAPId \_ da \_ SVCID \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="73b6d-123">Retorna o identificador SAP do NetWare associado ao GUID.</span><span class="sxs-lookup"><span data-stu-id="73b6d-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="73b6d-124">Essa macro é usada com o namespace do SAP em um ambiente do NetWare.</span><span class="sxs-lookup"><span data-stu-id="73b6d-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="73b6d-125">**é \_ SVCID \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="73b6d-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="73b6d-126">Retornará **true** se o GUID para NetWare estiver dentro do intervalo permitido.</span><span class="sxs-lookup"><span data-stu-id="73b6d-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="73b6d-127">Essa macro é usada com o namespace do SAP em um ambiente do NetWare.</span><span class="sxs-lookup"><span data-stu-id="73b6d-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="73b6d-128">O arquivo de cabeçalho *Svcguid. h* não é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="73b6d-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




