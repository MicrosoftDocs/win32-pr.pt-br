---
title: Localizando dispositivos
description: A arquitetura UPnP é uma arquitetura de rede dinâmica que permite que os dispositivos ingressem e saiam da rede a qualquer momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005983"
---
# <a name="finding-devices"></a><span data-ttu-id="b8f43-103">Localizando dispositivos</span><span class="sxs-lookup"><span data-stu-id="b8f43-103">Finding Devices</span></span>

<span data-ttu-id="b8f43-104">A arquitetura UPnP é uma arquitetura de rede dinâmica que permite que os dispositivos ingressem e saiam da rede a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b8f43-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="b8f43-105">Devido a essa arquitetura dinâmica, os aplicativos não podem depender de dispositivos baseados em UPnP específicos para que estejam disponíveis em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="b8f43-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="b8f43-106">Por esse motivo, os aplicativos (ou pontos de controle) pesquisam a rede para localizar os dispositivos que mais correspondam aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="b8f43-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="b8f43-107">Os aplicativos também esperam mensagens de anúncio de dispositivo que indicam que novos dispositivos foram adicionados à rede.</span><span class="sxs-lookup"><span data-stu-id="b8f43-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="b8f43-108">Estes são os critérios de pesquisa válidos para dispositivos baseados em UPnP:</span><span class="sxs-lookup"><span data-stu-id="b8f43-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="b8f43-109">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b8f43-109">Device type</span></span>
-   <span data-ttu-id="b8f43-110">Tipo de serviço</span><span class="sxs-lookup"><span data-stu-id="b8f43-110">Service type</span></span>
-   <span data-ttu-id="b8f43-111">Nome de dispositivo exclusivo (UDN)</span><span class="sxs-lookup"><span data-stu-id="b8f43-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="b8f43-112">Todos os dispositivos raiz</span><span class="sxs-lookup"><span data-stu-id="b8f43-112">All root devices</span></span>

<span data-ttu-id="b8f43-113">As pesquisas de tipo de dispositivo e de serviço normalmente são usadas para encontrar uma classe de dispositivos com características comuns.</span><span class="sxs-lookup"><span data-stu-id="b8f43-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="b8f43-114">A pesquisa UDN é usada para localizar um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="b8f43-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="b8f43-115">Para procurar dispositivos, um aplicativo deve primeiro instanciar o objeto do localizador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b8f43-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="b8f43-116">Esse objeto expõe a interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; seus métodos executam as pesquisas descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b8f43-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="b8f43-117">As seções a seguir descrevem o processo de localizar dispositivos:</span><span class="sxs-lookup"><span data-stu-id="b8f43-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="b8f43-118">Criando o localizador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="b8f43-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="b8f43-119">Pesquisa assíncrona</span><span class="sxs-lookup"><span data-stu-id="b8f43-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="b8f43-120">Pesquisa síncrona</span><span class="sxs-lookup"><span data-stu-id="b8f43-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="b8f43-121">Coleções de dispositivos retornadas por pesquisas síncronas</span><span class="sxs-lookup"><span data-stu-id="b8f43-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




