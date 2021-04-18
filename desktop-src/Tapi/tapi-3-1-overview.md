---
description: A TAPI versão 3,1 é uma API baseada em COM que mescla a telefonia clássica e IP. Os aplicativos possíveis variam de chamadas simples de voz pela PSTN (rede telefônica pública comutada) à conferência de IP de multimídia de multicast com QOS (qualidade de serviço).
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: Visão geral da TAPI 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779895"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="d6f73-104">Visão geral da TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d6f73-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="d6f73-105">A TAPI versão 3,1 é uma API baseada em COM que mescla a telefonia clássica e IP.</span><span class="sxs-lookup"><span data-stu-id="d6f73-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="d6f73-106">Os aplicativos possíveis variam de chamadas simples de voz pela PSTN (rede telefônica pública comutada) à conferência de IP de multimídia de multicast com QOS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="d6f73-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="d6f73-107">Para obter informações adicionais sobre os recursos de telefonia IP TAPI 3,1, consulte a "telefonia IP com TAPI 3" white paper, que pode ser encontrada no site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d6f73-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="d6f73-108">Há quatro componentes principais para a TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="d6f73-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="d6f73-109">API COM</span><span class="sxs-lookup"><span data-stu-id="d6f73-109">COM API</span></span>
-   <span data-ttu-id="d6f73-110">Servidor TAPI</span><span class="sxs-lookup"><span data-stu-id="d6f73-110">TAPI Server</span></span>
-   <span data-ttu-id="d6f73-111">Provedores de serviços de telefonia (TSPs)</span><span class="sxs-lookup"><span data-stu-id="d6f73-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="d6f73-112">Provedores de fluxo de mídia (MSPs)</span><span class="sxs-lookup"><span data-stu-id="d6f73-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="d6f73-113">O diagrama a seguir ilustra a arquitetura TAPI 3,1:</span><span class="sxs-lookup"><span data-stu-id="d6f73-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![arquitetura TAPI 3](images/callarc-gif-1.png)

<span data-ttu-id="d6f73-115">A API é implementada como um conjunto de objetos COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="d6f73-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="d6f73-116">Mover a TAPI para o modelo COM orientado a objeto permite que os desenvolvedores gravem aplicativos habilitados para TAPI em várias linguagens, como Java, Visual Basic ou C/C++.</span><span class="sxs-lookup"><span data-stu-id="d6f73-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="d6f73-117">O uso de COM habilita atualizações de componentes de recursos TAPI.</span><span class="sxs-lookup"><span data-stu-id="d6f73-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="d6f73-118">O processo do servidor TAPI (TAPISRV) abstrai a interface do provedor de serviços TAPI (TSPI) da TAPI 3. x e TAPI 2. x, permitindo que os provedores de serviços de telefonia TAPI 2. x sejam usados com a TAPI 3. x, mantendo o estado interno da TAPI.</span><span class="sxs-lookup"><span data-stu-id="d6f73-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="d6f73-119">O TAPISRV é implementado como um processo de serviço no SVCHOST.</span><span class="sxs-lookup"><span data-stu-id="d6f73-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="d6f73-120">[Provedores de serviço](./tapi-service-providers.md) abstratos mecanismos de transporte de mídia específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="d6f73-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="d6f73-121">Eles normalmente existem em pares – um provedor de serviços de telefonia (TSP) para controle de chamada e um provedor de serviços de mídia (MSP) para controle de mídia.</span><span class="sxs-lookup"><span data-stu-id="d6f73-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="d6f73-122">Os TSPs ( [provedores de serviços de telefonia](./telephony-service-providers-start-page.md) ) são responsáveis por resolver o modelo de chamada independente de protocolo da TAPI em mecanismos de controle de chamada específicos de protocolo.</span><span class="sxs-lookup"><span data-stu-id="d6f73-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="d6f73-123">A TAPI 3,1 fornece compatibilidade com versões anteriores do TAPI 2,1 TSPs.</span><span class="sxs-lookup"><span data-stu-id="d6f73-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="d6f73-124">Dois provedores de serviço de telefonia IP (e seus MSPs associados) são enviados por padrão com TAPI 3,1: o H. 323 TSP e o IP multicast Conferencing TSP.</span><span class="sxs-lookup"><span data-stu-id="d6f73-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="d6f73-125">Os [provedores de serviço de mídia](media-service-providers-start-page.md) (MSPs) fornecem uma maneira uniforme de acessar os fluxos de mídia em uma chamada, dando suporte à API do DirectShow<sup>TM</sup> como o manipulador de fluxo de mídia primário.</span><span class="sxs-lookup"><span data-stu-id="d6f73-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="d6f73-126">A TAPI MSPs implementa interfaces do DirectShow para um TSP específico e é necessária para qualquer serviço de telefonia que utiliza o streaming do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d6f73-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="d6f73-127">Os fluxos genéricos são tratados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6f73-127">Generic streams are handled by the application.</span></span>

 

 
