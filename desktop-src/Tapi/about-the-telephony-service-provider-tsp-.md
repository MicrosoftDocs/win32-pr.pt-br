---
description: Um provedor de serviços de telefonia TAPI (TSP) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Sobre o provedor de serviços de telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646972"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="2f8d4-103">Sobre o provedor de serviços de telefonia (TSP)</span><span class="sxs-lookup"><span data-stu-id="2f8d4-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="2f8d4-104">\[ O H323 e o IPConf TSPs não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f8d4-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2f8d4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2f8d4-106">Um provedor de serviços de telefonia TAPI (TSP) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="2f8d4-107">Um aplicativo TAPI usa comandos padronizados, a TAPI passa na formação de informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="2f8d4-108">As seções a seguir descrevem brevemente o TSPs fornecido com o Microsoft Windows:</span><span class="sxs-lookup"><span data-stu-id="2f8d4-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="2f8d4-109">H323 TSP</span><span class="sxs-lookup"><span data-stu-id="2f8d4-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="2f8d4-110">IPConf TSP</span><span class="sxs-lookup"><span data-stu-id="2f8d4-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="2f8d4-111">Driver de dispositivo no modo kernel TSP</span><span class="sxs-lookup"><span data-stu-id="2f8d4-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="2f8d4-112">TSP do proxy NDIS</span><span class="sxs-lookup"><span data-stu-id="2f8d4-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="2f8d4-113">TSP remoto</span><span class="sxs-lookup"><span data-stu-id="2f8d4-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="2f8d4-114">TSP de terceiros</span><span class="sxs-lookup"><span data-stu-id="2f8d4-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="2f8d4-115">Unimodem TSP</span><span class="sxs-lookup"><span data-stu-id="2f8d4-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="2f8d4-116">Para obter informações detalhadas, consulte o kit de recursos para o sistema operacional de destino.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="2f8d4-117">Os TSPs de terceiros para dispositivos de comunicação especializados normalmente serão fornecidos pelo fabricante e serão instalados com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="2f8d4-118">Os tópicos a seguir descrevem como criar um TSP que funcionará corretamente dentro do ambiente de telefonia da Microsoft e como criar um par de TSP/MSP:</span><span class="sxs-lookup"><span data-stu-id="2f8d4-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="2f8d4-119">Interface do provedor de serviços de telefonia (TSPI)</span><span class="sxs-lookup"><span data-stu-id="2f8d4-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="2f8d4-120">Referência de TSPI</span><span class="sxs-lookup"><span data-stu-id="2f8d4-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="2f8d4-121">Provedores de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="2f8d4-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="2f8d4-122">Um TSP é uma DLL criada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="2f8d4-123">Se você estiver criando um TSP para uma plataforma do Windows de 64 bits, deverá compilá-lo como uma DLL ou DLLs de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2f8d4-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
