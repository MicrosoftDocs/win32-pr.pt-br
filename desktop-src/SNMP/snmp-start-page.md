---
title: Serviço SNMP
description: A implementação do Microsoft Windows do Simple Network Management Protocol (SNMP) é usada para configurar dispositivos remotos, monitorar o desempenho da rede, auditar o uso da rede e detectar falhas de rede ou acesso impróprio. Importante a API SNMP do Microsoft Windows só dá suporte a versões de protocolo até o SNMPv2C. Ele não oferece suporte a nenhuma versão posterior do protocolo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP DO SNMP
- SNMP do SNMP, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008045"
---
# <a name="snmp-service"></a><span data-ttu-id="fcf61-106">Serviço SNMP</span><span class="sxs-lookup"><span data-stu-id="fcf61-106">SNMP Service</span></span>

<span data-ttu-id="fcf61-107">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fcf61-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fcf61-108">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fcf61-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fcf61-109">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="fcf61-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="fcf61-110">Finalidade</span><span class="sxs-lookup"><span data-stu-id="fcf61-110">Purpose</span></span>

<span data-ttu-id="fcf61-111">A implementação do Microsoft Windows do Simple Network Management Protocol (SNMP) é usada para configurar dispositivos remotos, monitorar o desempenho da rede, auditar o uso da rede e detectar falhas de rede ou acesso impróprio.</span><span class="sxs-lookup"><span data-stu-id="fcf61-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcf61-112">A API SNMP do Microsoft Windows só dá suporte a versões de protocolo até o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fcf61-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="fcf61-113">Ele não oferece suporte a nenhuma versão posterior do protocolo.</span><span class="sxs-lookup"><span data-stu-id="fcf61-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="fcf61-114">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="fcf61-114">Where applicable</span></span>

<span data-ttu-id="fcf61-115">O SNMP usa uma arquitetura distribuída que consiste em aplicativos de gerenciamento e aplicativos de agente.</span><span class="sxs-lookup"><span data-stu-id="fcf61-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="fcf61-116">O serviço SNMP implementa um agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="fcf61-117">Para usar as informações fornecidas pelo serviço SNMP, você deve ter pelo menos um host que esteja executando um aplicativo de gerenciamento SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="fcf61-118">Você pode usar software de gerenciamento SNMP de terceiros ou pode desenvolver seu próprio aplicativo de software de gerenciamento SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="fcf61-119">As seguintes APIs estão disponíveis para essa finalidade:</span><span class="sxs-lookup"><span data-stu-id="fcf61-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="fcf61-120">API de gerenciamento SNMP, um conjunto de funções que podem ser usadas para desenvolver rapidamente sistemas de gerenciamento SNMP básicos</span><span class="sxs-lookup"><span data-stu-id="fcf61-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="fcf61-121">API WinSNMP, versão 2,0, um conjunto de funções para codificação, decodificação, envio e recebimento de mensagens SNMP</span><span class="sxs-lookup"><span data-stu-id="fcf61-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="fcf61-122">Além disso, a API do agente de extensão SNMP define a interface entre o serviço SNMP e as DLLs do agente de extensão SNMP de terceiros.</span><span class="sxs-lookup"><span data-stu-id="fcf61-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="fcf61-123">As funções de API do utilitário SNMP podem ser usadas para simplificar o processamento de mensagens SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fcf61-124">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="fcf61-124">Developer audience</span></span>

<span data-ttu-id="fcf61-125">As APIs listadas na seção anterior foram projetadas para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="fcf61-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="fcf61-126">É necessário ter familiaridade com o SNMP e o SNMPv2C, bem como um conhecimento prático de conceitos de rede e de gerenciamento de rede.</span><span class="sxs-lookup"><span data-stu-id="fcf61-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fcf61-127">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="fcf61-127">Run-time requirements</span></span>

<span data-ttu-id="fcf61-128">Para obter mais informações sobre o sistema operacional necessário para usar uma função específica, consulte a seção requisitos da página de referência para essa função.</span><span class="sxs-lookup"><span data-stu-id="fcf61-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fcf61-129">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fcf61-129">In this section</span></span>



| <span data-ttu-id="fcf61-130">Tópico</span><span class="sxs-lookup"><span data-stu-id="fcf61-130">Topic</span></span>                                                                                                | <span data-ttu-id="fcf61-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcf61-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcf61-132">Novidades no SNMP</span><span class="sxs-lookup"><span data-stu-id="fcf61-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="fcf61-133">Informações sobre atualizações do SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="fcf61-134">Protocolo SNMP</span><span class="sxs-lookup"><span data-stu-id="fcf61-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="fcf61-135">Referência de API e informações para SNMP, incluindo a API de gerenciamento SNMP, a API do agente de extensão SNMP e as funções de API do utilitário SNMP.</span><span class="sxs-lookup"><span data-stu-id="fcf61-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="fcf61-136">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="fcf61-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="fcf61-137">Informações e referência de API para a interface de programação de aplicativo do Microsoft Windows SNMP (API WinSNMP).</span><span class="sxs-lookup"><span data-stu-id="fcf61-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="fcf61-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcf61-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcf61-139">Protocolo DHCP</span><span class="sxs-lookup"><span data-stu-id="fcf61-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="fcf61-140">Gerenciamento de rede</span><span class="sxs-lookup"><span data-stu-id="fcf61-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="fcf61-141">Serviço de Roteamento e Acesso Remoto</span><span class="sxs-lookup"><span data-stu-id="fcf61-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

