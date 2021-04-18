---
title: Descobrir dispositivos e serviços Bluetooth
description: Para facilitar a descoberta de dispositivos e serviços Bluetooth, o Windows mapeia o protocolo de descoberta de serviço do Bluetooth (SDP) para as interfaces de namespace do Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tarefas, descobrindo dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2020
ms.locfileid: "105756467"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="ded91-104">Descobrir dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="ded91-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="ded91-105">Para facilitar a descoberta de dispositivos e serviços Bluetooth, o Windows mapeia o protocolo de descoberta de serviço do Bluetooth (SDP) para as interfaces de namespace do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="ded91-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="ded91-106">As funções primárias usadas para esse mapeamento são as funções [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="ded91-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="ded91-107">A estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) também é usada em conjunto com essas funções.</span><span class="sxs-lookup"><span data-stu-id="ded91-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="ded91-108">Como determinados conceitos e parâmetros do SDP do Bluetooth não são necessariamente mapeados diretamente para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , a atenção deve ser paga sobre como seus membros são criados e usados.</span><span class="sxs-lookup"><span data-stu-id="ded91-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="ded91-109">Para muitas operações de Bluetooth complexas, como a criação de registros SDP, o membro **lpBlob** do **WSAQUERYSET** é usado.</span><span class="sxs-lookup"><span data-stu-id="ded91-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="ded91-110">Quando essa consideração especial é necessária, ela é descrita especificamente, como em páginas de referência como [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre outras.</span><span class="sxs-lookup"><span data-stu-id="ded91-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="ded91-111">É importante entender que o registro SDP é separado do controle de soquete.</span><span class="sxs-lookup"><span data-stu-id="ded91-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="ded91-112">Quando um aplicativo de servidor está preparado para aceitar a conexão do cliente, ele deve chamar a função [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar um registro SDP do Bluetooth que corresponda a esse serviço.</span><span class="sxs-lookup"><span data-stu-id="ded91-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="ded91-113">Esse aplicativo Bluetooth deve chamar a função **WSASetService** novamente antes de fechar, para cancelar o registro de registros de SDP do Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ded91-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="ded91-114">Ao usar as funções de mapeamento descritas nesta página, o \_ namespace NS BTH é atribuído.</span><span class="sxs-lookup"><span data-stu-id="ded91-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="ded91-115">Para obter mais informações sobre como descobrir dispositivos e serviços, consulte as seguintes páginas de referência:</span><span class="sxs-lookup"><span data-stu-id="ded91-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="ded91-116">**Bluetooth e WSASetService**</span><span class="sxs-lookup"><span data-stu-id="ded91-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="ded91-117">**Bluetooth e WSALookupServiceBegin para consulta de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ded91-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="ded91-118">**Bluetooth e WSALookupServiceBegin para descoberta de serviço**</span><span class="sxs-lookup"><span data-stu-id="ded91-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="ded91-119">**Bluetooth e WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="ded91-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="ded91-120">**Bluetooth e WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="ded91-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="ded91-121">**Bluetooth e BLOB**</span><span class="sxs-lookup"><span data-stu-id="ded91-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="ded91-122">**Bluetooth e WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="ded91-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="ded91-123">Você também pode baixar o [exemplo de conexão Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obter um exemplo completo.</span><span class="sxs-lookup"><span data-stu-id="ded91-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ded91-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ded91-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ded91-125">Programação de Bluetooth com Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ded91-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="ded91-126">Exemplo de conexão Bluetooth</span><span class="sxs-lookup"><span data-stu-id="ded91-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




