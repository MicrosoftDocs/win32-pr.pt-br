---
description: Glossário de Monitor de Rede termos que começam com a letra N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Monitor de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829339"
---
# <a name="n-network-monitor"></a><span data-ttu-id="2a72b-103">N (Monitor de Rede)</span><span class="sxs-lookup"><span data-stu-id="2a72b-103">N (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="2a72b-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**RECEPÇÃO**</span><span class="sxs-lookup"><span data-stu-id="2a72b-104"><span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-105">Consulte especificação da interface do driver de rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-105">See network driver interface specification.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**NDIS (especificação de interface de driver de rede)**</span><span class="sxs-lookup"><span data-stu-id="2a72b-106"><span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**network driver interface specification (NDIS)**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-107">A especificação para a interface entre drivers de dispositivo e uma rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-107">The specification for the interface between device drivers and a network.</span></span> <span data-ttu-id="2a72b-108">Todos os transportes chamam a interface NDIS para acessar e trabalhar com placas de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-108">All transports call the NDIS interface to access and work with network interface cards.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agente de Monitor de Rede**</span><span class="sxs-lookup"><span data-stu-id="2a72b-109"><span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Network Monitor agent**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-110">Um componente Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-110">A Network Monitor component.</span></span> <span data-ttu-id="2a72b-111">O agente permite que um computador remoto Capture dados da rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-111">The agent enables a remote computer to capture data from the network.</span></span> <span data-ttu-id="2a72b-112">Quando uma instalação do Monitor de Rede se conecta remotamente ao agente de Monitor de Rede e inicia uma captura, as estatísticas da captura são transferidas pela rede para o computador de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="2a72b-112">When a Network Monitor installation connects remotely to the Network Monitor agent and initiates a capture, statistics from the capture are transferred over the network to the managing computer.</span></span> <span data-ttu-id="2a72b-113">A transferência continua em intervalos especificados quando a conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="2a72b-113">The transfer proceeds at intervals specified when the connection is made.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**provedor de pacotes de rede (NPP)**</span><span class="sxs-lookup"><span data-stu-id="2a72b-114"><span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**network packet provider (NPP)**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-115">O componente Monitor de Rede que coleta o tráfego de rede em quadros e, em seguida, passa os quadros para um especialista e o aplicativo NPP.</span><span class="sxs-lookup"><span data-stu-id="2a72b-115">The Network Monitor component that collects network traffic in frames, and then passes the frames to an expert, and NPP application.</span></span> <span data-ttu-id="2a72b-116">Um NPP usa o Nmnt.sys (driver de sistema Monitor de Rede) para obter os quadros coletados da rede e fornece várias interfaces COM que passam os quadros para um aplicativo de especialista, monitor e provedor de pacotes de rede (NPP), no qual eles podem ser exibidos e analisados.</span><span class="sxs-lookup"><span data-stu-id="2a72b-116">An NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network, and provides several COM interfaces that pass the frames to an expert, monitor, and network packet provider (NPP) application where they can be displayed and analyzed.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span><span class="sxs-lookup"><span data-stu-id="2a72b-117"><span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-118">Consulte provedor de pacotes de rede.</span><span class="sxs-lookup"><span data-stu-id="2a72b-118">See network packet provider.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Aplicativo NPP**</span><span class="sxs-lookup"><span data-stu-id="2a72b-119"><span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**NPP application**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-120">Um aplicativo que ignora o Monitor de Rede interface do usuário e a ferramenta de controle de monitor e conecta-se diretamente ao provedor de pacotes de rede (NPP).</span><span class="sxs-lookup"><span data-stu-id="2a72b-120">An application that bypasses both the Network Monitor UI and Monitor Control Tool, and connects directly to the network packet provider (NPP).</span></span> <span data-ttu-id="2a72b-121">Um aplicativo NPP pode se conectar ao componente NPP com qualquer uma das cinco interfaces COM do NPP.</span><span class="sxs-lookup"><span data-stu-id="2a72b-121">An NPP application can connect to the NPP component with any of the five NPP COM interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="2a72b-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Localizador de NPP**</span><span class="sxs-lookup"><span data-stu-id="2a72b-122"><span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**NPP Finder**</span></span>
</dt> <dd>

<span data-ttu-id="2a72b-123">O componente Monitor de Rede que se comunica com o NPPs.</span><span class="sxs-lookup"><span data-stu-id="2a72b-123">The Network Monitor component that communicates with NPPs.</span></span>

</dd> </dl>

 

 



