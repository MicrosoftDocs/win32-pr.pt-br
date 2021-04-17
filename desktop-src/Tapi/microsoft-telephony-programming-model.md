---
description: O modelo de programação de telefonia da Microsoft abstrai o controle de comunicação do controle de dispositivo, liberando aplicativos de usuário final e fabricantes de dispositivos da necessidade de março no atrelada.
ms.assetid: 07dd8447-08dc-4ae3-9a22-70e914c392db
title: Modelo de programação de telefonia da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efb8947f3b428ab4a252301e3fdd5f94e29f6ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761350"
---
# <a name="microsoft-telephony-programming-model"></a><span data-ttu-id="aa303-103">Modelo de programação de telefonia da Microsoft</span><span class="sxs-lookup"><span data-stu-id="aa303-103">Microsoft Telephony Programming Model</span></span>

<span data-ttu-id="aa303-104">O modelo de programação de telefonia da Microsoft abstrai o controle de comunicação do controle de dispositivo, liberando aplicativos de usuário final e fabricantes de dispositivos da necessidade de março no atrelada.</span><span class="sxs-lookup"><span data-stu-id="aa303-104">The Microsoft Telephony programming model abstracts communications control from device control, freeing end-user applications and device manufacturers from the need to march in lockstep.</span></span> <span data-ttu-id="aa303-105">Usando esse modelo, um usuário final ou um aplicativo de servidor não requer informações detalhadas sobre o controle de dispositivo e o dispositivo não precisa ser ajustado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa303-105">Using this model, an end-user or server application does not require detailed information on device control and the device does not need to be tailored to the application.</span></span> <span data-ttu-id="aa303-106">Aplicativos e dispositivos podem passar por inovações e alterações sem renderizar outros inúteis para os clientes.</span><span class="sxs-lookup"><span data-stu-id="aa303-106">Applications and devices can undergo innovation and change without rendering each other useless to customers.</span></span>

<span data-ttu-id="aa303-107">O diagrama a seguir ilustra como essa abstração é realizada.</span><span class="sxs-lookup"><span data-stu-id="aa303-107">The following diagram illustrates how this abstraction is accomplished.</span></span>

![como a TAPI abstrai o controle de comunicação do controle de dispositivo](images/tapicomp.png)

<span data-ttu-id="aa303-109">Esses componentes podem ser exibidos como repositórios de conhecimento especializado.</span><span class="sxs-lookup"><span data-stu-id="aa303-109">These components can be viewed as repositories of specialized knowledge.</span></span> <span data-ttu-id="aa303-110">O aplicativo da TAPI (interface de programação de aplicativo) de telefonia sabe que as necessidades do usuário, a DLL de TAPI e o TAPISRV entendem a telefonia geral e os provedores de serviços (TSP e MSP) sabem controle de dispositivo detalhado.</span><span class="sxs-lookup"><span data-stu-id="aa303-110">The Telephony Application Programming Interface (TAPI) application knows user needs, the TAPI DLL and TAPISRV understand general telephony, and the service providers (TSP and MSP) know detailed device control.</span></span> <span data-ttu-id="aa303-111">Os desenvolvedores de aplicativos e os fabricantes de dispositivos exigem apenas conhecimento geral dos requisitos uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="aa303-111">Application writers and device manufacturers require only general knowledge of each other's requirements.</span></span>

-   <span data-ttu-id="aa303-112">Um aplicativo carrega a DLL TAPI em seu espaço de processo e usa a TAPI para comunicar as necessidades.</span><span class="sxs-lookup"><span data-stu-id="aa303-112">An application loads the TAPI DLL into its process space and uses TAPI to communicate needs.</span></span>
-   <span data-ttu-id="aa303-113">A TAPI estabelece uma comunicação de link RPC com o servidor TAPI.</span><span class="sxs-lookup"><span data-stu-id="aa303-113">TAPI establishes an RPC link communications with the TAPI Server.</span></span>
-   <span data-ttu-id="aa303-114">Além disso, a TAPI 3. x cria um objeto MSP e se comunica com ele usando um conjunto definido de comandos, a MSPI (interface do provedor de serviços de mídia).</span><span class="sxs-lookup"><span data-stu-id="aa303-114">In addition, TAPI 3.x creates an MSP object and communicates with it using a defined set of commands, the Media Service Provider Interface (MSPI).</span></span>
-   <span data-ttu-id="aa303-115">Quando um aplicativo chama uma operação TAPI, a biblioteca de vínculo dinâmico TAPI valida e realiza marshaling dos parâmetros e, em seguida, encaminha as informações para TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="aa303-115">When an application calls a TAPI operation, the TAPI dynamic-link library validates and marshals the parameters, then forwards the information to TAPISRV.</span></span>
-   <span data-ttu-id="aa303-116">O TAPISRV rastreia os recursos de comunicação disponíveis para o computador local e as interfaces com os provedores de serviços de telefonia (TSPs) usando a interface do provedor de serviços de telefonia (TSPI).</span><span class="sxs-lookup"><span data-stu-id="aa303-116">TAPISRV tracks communications resources available to the local machine and interfaces with the Telephony Service Providers (TSPs) using the Telephony Service Provider Interface (TSPI).</span></span>
-   <span data-ttu-id="aa303-117">As comunicações entre um TSP e um MSP ocorrem usando uma conexão virtual que passa pela DLL de TAPI e TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="aa303-117">Communications between a TSP and an MSP take place using a virtual connection that passes through the TAPI DLL and TAPISRV.</span></span>
-   <span data-ttu-id="aa303-118">O par de TSP/MSP fornece informações sobre o estado do dispositivo e os recursos e implementa os comandos específicos necessários para uma resposta desejada.</span><span class="sxs-lookup"><span data-stu-id="aa303-118">The TSP/MSP pair supplies information on device state and capabilities and implements the specific commands required for a desired response.</span></span>

<span data-ttu-id="aa303-119">O resultado do uso desse modelo de programação é que os aplicativos podem ignorar ou ajustar às alterações do dispositivo, e novos dispositivos podem ser instantaneamente úteis em vez de aguardar as alterações na base do código.</span><span class="sxs-lookup"><span data-stu-id="aa303-119">The result of using this programming model is that applications can ignore or adjust to device changes and new devices can be instantly useful instead of waiting on code base changes.</span></span> <span data-ttu-id="aa303-120">A possível participação no mercado é expandida para os desenvolvedores de aplicativos e para os fabricantes de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa303-120">Potential market share is expanded for both application writers and device manufacturers.</span></span>

<span data-ttu-id="aa303-121">Os tópicos a seguir descrevem os componentes de telefonia da Microsoft com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="aa303-121">The following topics describe the Microsoft Telephony components in more detail:</span></span>

-   [<span data-ttu-id="aa303-122">Aplicativos TAPI</span><span class="sxs-lookup"><span data-stu-id="aa303-122">TAPI Applications</span></span>](tapi-applications.md)
-   [<span data-ttu-id="aa303-123">DLL TAPI</span><span class="sxs-lookup"><span data-stu-id="aa303-123">TAPI DLL</span></span>](tapi-dll.md)
-   [<span data-ttu-id="aa303-124">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="aa303-124">TAPI Server</span></span>](tapi-server.md)
-   [<span data-ttu-id="aa303-125">Provedores de serviço</span><span class="sxs-lookup"><span data-stu-id="aa303-125">Service Providers</span></span>](service-providers.md)
-   [<span data-ttu-id="aa303-126">Modelo síncrono/assíncrono</span><span class="sxs-lookup"><span data-stu-id="aa303-126">Synchronous/Asynchronous Model</span></span>](synchronous-asynchronous-model.md)
-   [<span data-ttu-id="aa303-127">Estruturas de dados TAPI</span><span class="sxs-lookup"><span data-stu-id="aa303-127">TAPI Data Structures</span></span>](tapi-data-structures.md)
-   [<span data-ttu-id="aa303-128">Níveis de serviço TAPI</span><span class="sxs-lookup"><span data-stu-id="aa303-128">TAPI Levels of Service</span></span>](tapi-levels-of-service.md)

 

 



