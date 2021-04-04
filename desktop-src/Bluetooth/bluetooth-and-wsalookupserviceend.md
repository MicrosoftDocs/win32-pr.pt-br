---
title: Bluetooth e WSALookupServiceEnd
description: O Bluetooth usa a função WSALookupServiceEnd para encerrar uma consulta iniciada em uma chamada anterior para WSALookupServiceBegin e, talvez, estendida em chamadas subsequentes para WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917390"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="84766-106">Bluetooth e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="84766-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="84766-107">O Bluetooth usa a função [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para encerrar uma consulta iniciada em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e, talvez, estendida em chamadas subsequentes para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="84766-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="84766-108">A chamada para **WSALookupServiceEnd** encerra a consulta e limpa o contexto.</span><span class="sxs-lookup"><span data-stu-id="84766-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="84766-109">As etapas para a consulta do dispositivo e a descoberta de serviço no Bluetooth são suficientemente diferentes para mérito um tratamento separado.</span><span class="sxs-lookup"><span data-stu-id="84766-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="84766-110">Para obter mais informações sobre o Bluetooth e a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivo, consulte [Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="84766-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="84766-111">Para obter mais informações sobre o Bluetooth e a função **WSALookupServiceBegin** para descoberta de serviço, consulte [Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="84766-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84766-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84766-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84766-113">Descobrir dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="84766-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="84766-114">Bluetooth e WSALookupServiceBegin para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="84766-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="84766-115">Bluetooth e WSALookupServiceBegin para descoberta de serviço</span><span class="sxs-lookup"><span data-stu-id="84766-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="84766-116">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="84766-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="84766-117">**\_serviço de consulta do BTH \_**</span><span class="sxs-lookup"><span data-stu-id="84766-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="84766-118">**conectar**</span><span class="sxs-lookup"><span data-stu-id="84766-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="84766-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="84766-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="84766-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="84766-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="84766-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="84766-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="84766-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="84766-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="84766-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="84766-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="84766-124">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="84766-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 