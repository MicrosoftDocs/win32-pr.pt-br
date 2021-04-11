---
description: Monitor de Rede é um componente do Microsoft Systems Management Server (SMS) usado para detectar e solucionar problemas em LANs, WANs e Links seriais que executam o Microsoft Remote Access Server (RAS).
ms.assetid: bd273439-daa2-4263-8f12-28ec988beea0
title: Sobre o Monitor de Rede 2,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447f4763e0c73dc0dcac4cf719a0bad4b61f073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010988"
---
# <a name="about-network-monitor-21"></a><span data-ttu-id="d056d-103">Sobre o Monitor de Rede 2,1</span><span class="sxs-lookup"><span data-stu-id="d056d-103">About Network Monitor 2.1</span></span>

<span data-ttu-id="d056d-104">Monitor de Rede é um componente do Microsoft Systems Management Server (SMS) usado para detectar e solucionar problemas em LANs, WANs e Links seriais que executam o Microsoft Remote Access Server (RAS).</span><span class="sxs-lookup"><span data-stu-id="d056d-104">Network Monitor is a component of Microsoft Systems Management Server (SMS) used to detect and troubleshoot problems on LANs, WANs, and serial links running Microsoft Remote Access Server (RAS).</span></span> <span data-ttu-id="d056d-105">O Monitor de Rede fornece análise de dados de rede após a captura.</span><span class="sxs-lookup"><span data-stu-id="d056d-105">Network Monitor provides post-capture network data analysis.</span></span>

<span data-ttu-id="d056d-106">Na análise após a captura, o tráfego de rede é salvo em um arquivo de captura proprietário, para que os dados capturados possam ser analisados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d056d-106">In post-capture analysis, network traffic is saved in a proprietary capture file, so that the captured data can be analyzed later.</span></span> <span data-ttu-id="d056d-107">Nesse caso, a análise pode estar na forma de [*analisadores*](p.md) de protocolo que selecionam tipos de quadro de rede específicos e exibindo os dados de quadro na interface do usuário do monitor de rede; ou a análise pode estar na forma de [*especialistas*](e.md) examinando os dados da rede e exibindo um relatório (os especialistas também podem manipular os dados da rede).</span><span class="sxs-lookup"><span data-stu-id="d056d-107">In this case, analysis can be in the form of protocol [*parsers*](p.md) picking out specific network frame types and displaying the frame data in the Network Monitor UI; or analysis can be in the form of [*experts*](e.md) examining the network data and displaying a report (experts may also manipulate the network data).</span></span>

<span data-ttu-id="d056d-108">Monitor de Rede fornece os seguintes tipos de funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="d056d-108">Network Monitor provides the following types of functionality:</span></span>

-   <span data-ttu-id="d056d-109">Captura dados de rede em modo em tempo real ou atrasado.</span><span class="sxs-lookup"><span data-stu-id="d056d-109">Captures network data in real-time or delayed mode.</span></span>
-   <span data-ttu-id="d056d-110">Fornece recursos de filtragem ao capturar dados.</span><span class="sxs-lookup"><span data-stu-id="d056d-110">Provides filtering capabilities when capturing data.</span></span>
-   <span data-ttu-id="d056d-111">Usa especialistas e analisadores para análise detalhada posterior à captura.</span><span class="sxs-lookup"><span data-stu-id="d056d-111">Uses experts and parsers for detailed post-capture analysis.</span></span>

<span data-ttu-id="d056d-112">Para obter mais informações sobre Monitor de Rede recursos, consulte:</span><span class="sxs-lookup"><span data-stu-id="d056d-112">For more information about Network Monitor features, see:</span></span>

-   [<span data-ttu-id="d056d-113">Arquitetura de expert e parser</span><span class="sxs-lookup"><span data-stu-id="d056d-113">Expert and Parser Architecture</span></span>](expert-and-parser-architecture.md)
-   [<span data-ttu-id="d056d-114">Especialistas</span><span class="sxs-lookup"><span data-stu-id="d056d-114">Experts</span></span>](experts.md)
-   [<span data-ttu-id="d056d-115">Analisadores</span><span class="sxs-lookup"><span data-stu-id="d056d-115">Parsers</span></span>](parsers.md)
-   [<span data-ttu-id="d056d-116">Provedores de pacotes de rede</span><span class="sxs-lookup"><span data-stu-id="d056d-116">Network Packet Providers</span></span>](network-packet-providers.md)
-   [<span data-ttu-id="d056d-117">BLOBs de Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="d056d-117">Network Monitor BLOBs</span></span>](network-monitor-blobs.md)
-   [<span data-ttu-id="d056d-118">Página referência de evento</span><span class="sxs-lookup"><span data-stu-id="d056d-118">Event Reference Page</span></span>](event-reference-page.md)
-   [<span data-ttu-id="d056d-119">Filtros de captura</span><span class="sxs-lookup"><span data-stu-id="d056d-119">Capture Filters</span></span>](capture-filters.md)

<span data-ttu-id="d056d-120">**Windows Vista:** Monitor de Rede 2,1 e anteriores não têm suporte nesta plataforma.</span><span class="sxs-lookup"><span data-stu-id="d056d-120">**Windows Vista:** Network Monitor 2.1 and earlier are not supported on this platform.</span></span>

 

 



