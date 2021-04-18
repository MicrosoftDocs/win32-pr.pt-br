---
title: Bluetooth e BLOB
description: O Bluetooth usa a estrutura de BLOB para passar ou receber dados específicos de transporte para a estrutura WSAQUERYSET durante chamadas para as funções WSASetService ou WSALookupService.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753000"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="866be-107">Bluetooth e BLOB</span><span class="sxs-lookup"><span data-stu-id="866be-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="866be-108">O Bluetooth usa a estrutura de [**blob**](/windows/desktop/api/nspapi/ns-nspapi-blob) para passar ou receber dados específicos de transporte para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante chamadas para as funções [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* .</span><span class="sxs-lookup"><span data-stu-id="866be-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="866be-109">Para uso com o Bluetooth e a função [**WSASetService**](bluetooth-and-wsasetservice.md) , os membros da estrutura de [**BLOBs**](/windows/desktop/api/nspapi/ns-nspapi-blob) devem ter as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="866be-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="866be-110">O membro **cbSize** deve ser definido como o tamanho da estrutura [**de \_ \_ serviço do conjunto de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) usado no membro **pBlobData** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="866be-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="866be-111">O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ serviço de conjunto de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="866be-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="866be-112">Para usar com Bluetooth e [WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="866be-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="866be-113">O membro **cbSize** deve ser definido como o tamanho da estrutura [**de \_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) usada no membro **pBlobData** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="866be-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="866be-114">O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .</span><span class="sxs-lookup"><span data-stu-id="866be-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="866be-115">Para usar com o Bluetooth e o [WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use as seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="866be-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="866be-116">O membro **cbSize** deve ser definido como o tamanho da estrutura [**do \_ \_ serviço de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) usada no membro **pBlobData** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="866be-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="866be-117">O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ serviço de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .</span><span class="sxs-lookup"><span data-stu-id="866be-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="866be-118">Para obter mais informações, consulte a seção comentários na página de referência da estrutura de [**\_ \_ serviço do BTH Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="866be-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="866be-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="866be-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866be-120">Bluetooth e WSALookupServiceBegin para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="866be-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="866be-121">Bluetooth e WSALookupServiceBegin para descoberta de serviço</span><span class="sxs-lookup"><span data-stu-id="866be-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="866be-122">Bluetooth e WSASetService</span><span class="sxs-lookup"><span data-stu-id="866be-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="866be-123">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="866be-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="866be-124">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="866be-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="866be-125">**\_dispositivo de consulta BTH \_**</span><span class="sxs-lookup"><span data-stu-id="866be-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="866be-126">**\_serviço de consulta do BTH \_**</span><span class="sxs-lookup"><span data-stu-id="866be-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="866be-127">**BTH \_ definir \_ serviço**</span><span class="sxs-lookup"><span data-stu-id="866be-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="866be-128">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="866be-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="866be-129">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="866be-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="866be-130">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="866be-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 