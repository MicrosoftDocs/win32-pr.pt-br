---
title: Bluetooth e WSALookupServiceNext
description: O Bluetooth usa a função WSALookupServiceNext para fazer a correspondência de consultas especificadas em uma chamada anterior para WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823796"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="12e71-106">Bluetooth e WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="12e71-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="12e71-107">O Bluetooth usa a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para fazer a correspondência de consultas especificadas em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span><span class="sxs-lookup"><span data-stu-id="12e71-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="12e71-108">Os resultados da função **WSALookupServiceNext** são determinados pelas configurações definidas na estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passada na chamada de função **WSALookupServiceBegin** inicial.</span><span class="sxs-lookup"><span data-stu-id="12e71-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="12e71-109">As etapas para a consulta do dispositivo e a descoberta de serviço no Bluetooth são suficientemente diferentes para mérito um tratamento separado.</span><span class="sxs-lookup"><span data-stu-id="12e71-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="12e71-110">Para obter mais informações sobre o Bluetooth e a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivo, consulte [Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span><span class="sxs-lookup"><span data-stu-id="12e71-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="12e71-111">Para obter mais informações sobre o Bluetooth e a função **WSALookupServiceBegin** para descoberta de serviço, consulte [Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="12e71-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12e71-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12e71-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e71-113">Descobrir dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="12e71-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="12e71-114">Bluetooth e WSALookupServiceBegin para consulta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="12e71-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="12e71-115">Bluetooth e WSALookupServiceBegin para descoberta de serviço</span><span class="sxs-lookup"><span data-stu-id="12e71-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="12e71-116">Bluetooth e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="12e71-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="12e71-117">**\_serviço de consulta do BTH \_**</span><span class="sxs-lookup"><span data-stu-id="12e71-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="12e71-118">**conectar**</span><span class="sxs-lookup"><span data-stu-id="12e71-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="12e71-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="12e71-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="12e71-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="12e71-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="12e71-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="12e71-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="12e71-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="12e71-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="12e71-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="12e71-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 