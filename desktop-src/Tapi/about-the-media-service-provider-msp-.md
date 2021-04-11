---
description: Um MSP (provedor de serviços de mídia) da TAPI 3 permite um controle considerável do aplicativo sobre a mídia para um mecanismo de transporte específico.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Sobre o MSP (provedor de serviços de mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091873"
---
# <a name="about-the-media-service-provider-msp"></a><span data-ttu-id="62294-103">Sobre o MSP (provedor de serviços de mídia)</span><span class="sxs-lookup"><span data-stu-id="62294-103">About the Media Service Provider (MSP)</span></span>

<span data-ttu-id="62294-104">Um MSP (provedor de serviços de mídia) da TAPI 3 permite um controle considerável do aplicativo sobre a mídia para um mecanismo de transporte específico.</span><span class="sxs-lookup"><span data-stu-id="62294-104">A TAPI 3 media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="62294-105">Um MSP sempre existe emparelhado com um provedor de serviços de telefonia (TSP).</span><span class="sxs-lookup"><span data-stu-id="62294-105">An MSP always exists paired with a Telephony Service Provider (TSP).</span></span> <span data-ttu-id="62294-106">Assim como um TSP é uma camada de abstração para o controle de chamada, o MSP controla a mídia sem a necessidade de codificação específica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62294-106">Just as a TSP is an abstraction layer for call control, the MSP controls media without need for device-specific coding.</span></span> <span data-ttu-id="62294-107">Para obter um exemplo de comunicação MSP/TSP, consulte [visão geral do provedor de serviços TAPI](./tapi-service-provider-overview.md).</span><span class="sxs-lookup"><span data-stu-id="62294-107">For an example of MSP/TSP communication, see [TAPI Service Provider Overview](./tapi-service-provider-overview.md).</span></span>

<span data-ttu-id="62294-108">Um MSP permite o controle de mídia por meio do uso de interfaces especiais de terminal, Stream e substream definidas pela TAPI.</span><span class="sxs-lookup"><span data-stu-id="62294-108">An MSP enables media control through the use of special terminal, stream, and substream interfaces defined by TAPI.</span></span> <span data-ttu-id="62294-109">O diagrama em [sobre controles de mídia e de chamada](about-call-and-media-controls.md) ilustra como essas interfaces aparecem para um aplicativo TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="62294-109">The diagram in [About Call and Media Controls](about-call-and-media-controls.md) illustrates how these interfaces appear to a TAPI 3 application.</span></span>

<span data-ttu-id="62294-110">Além disso, um MSP pode implementar [interfaces específicas de provedor](provider-specific-interfaces.md)privada, que a TAPI agregará aos objetos padrão expostos a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62294-110">In addition, an MSP may implement private [provider-specific interfaces](provider-specific-interfaces.md), which TAPI will aggregate onto the standard objects exposed to an application.</span></span> <span data-ttu-id="62294-111">Por exemplo, o Microsoft IPConf MSP, que é instalado com o Microsoft Windows 2000, implementa a interface [**ITParticipant**](itparticipant.md) , que fornece controles para membros individuais de uma conferência.</span><span class="sxs-lookup"><span data-stu-id="62294-111">For example, the Microsoft IPConf MSP, which is installed with Microsoft Windows 2000, implements the [**ITParticipant**](itparticipant.md) interface, which provides controls for individual members of a conference.</span></span>

<span data-ttu-id="62294-112">O tópico a seguir descreve brevemente o MSPs que pode ser instalado com um sistema operacional da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62294-112">The following topic briefly describes the MSPs that may be installed with a Microsoft operating system.</span></span> <span data-ttu-id="62294-113">Para obter detalhes sobre a configuração e o uso, consulte o kit de recursos para a plataforma de destino.</span><span class="sxs-lookup"><span data-stu-id="62294-113">For details on configuration and usage, see the resource kit for the target platform.</span></span>

<span data-ttu-id="62294-114">Provedores de serviço de mídia de terceiros adicionais podem ser gravados para protocolos específicos ou para dispositivos físicos.</span><span class="sxs-lookup"><span data-stu-id="62294-114">Additional third-party media service providers can be written for particular protocols or for physical devices.</span></span> <span data-ttu-id="62294-115">A [MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-.md) descreve as interfaces que devem ser implementadas para permitir que um MSP interaja com os componentes da telefonia da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62294-115">The [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) describes the interfaces that must be implemented to allow an MSP to interact with the components of Microsoft Telephony.</span></span>

 

 
