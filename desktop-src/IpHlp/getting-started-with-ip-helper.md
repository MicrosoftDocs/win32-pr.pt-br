---
description: Veja a seguir um guia passo a passo para a programação de introdução usando a API (interface de programação de aplicativo) auxiliar de IP. Ele foi projetado para fornecer uma compreensão das funções auxiliares de IP e estruturas de dados básicas e como elas funcionam juntas.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introdução com auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837414"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="9ba24-104">Introdução com auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="9ba24-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="9ba24-105">Veja a seguir um guia passo a passo para a programação de introdução usando a API (interface de programação de aplicativo) auxiliar de IP.</span><span class="sxs-lookup"><span data-stu-id="9ba24-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="9ba24-106">Ele foi projetado para fornecer uma compreensão das funções auxiliares de IP e estruturas de dados básicas e como elas funcionam juntas.</span><span class="sxs-lookup"><span data-stu-id="9ba24-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="9ba24-107">O aplicativo usado para ilustração é um aplicativo auxiliar de IP muito básico.</span><span class="sxs-lookup"><span data-stu-id="9ba24-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="9ba24-108">Exemplos de código mais avançados estão incluídos nos exemplos incluídos no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9ba24-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="9ba24-109">A primeira etapa é a mesma para a maioria dos aplicativos auxiliares de IP.</span><span class="sxs-lookup"><span data-stu-id="9ba24-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="9ba24-110">Criando um aplicativo auxiliar de IP básico</span><span class="sxs-lookup"><span data-stu-id="9ba24-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="9ba24-111">As seções a seguir descrevem as etapas restantes para criar esse aplicativo auxiliar de IP básico.</span><span class="sxs-lookup"><span data-stu-id="9ba24-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="9ba24-112">Recuperando informações usando GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="9ba24-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="9ba24-113">Gerenciando adaptadores de rede usando o GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="9ba24-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="9ba24-114">Gerenciando interfaces usando o GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="9ba24-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="9ba24-115">Gerenciando endereços IP usando GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="9ba24-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="9ba24-116">Gerenciando concessões DHCP usando IpReleaseAddress e IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="9ba24-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="9ba24-117">Gerenciando endereços IP usando AddIPAddress e DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="9ba24-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="9ba24-118">Recuperando informações usando GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="9ba24-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="9ba24-119">Recuperando informações usando GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="9ba24-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="9ba24-120">O código-fonte completo para este exemplo de auxiliar de IP básico.</span><span class="sxs-lookup"><span data-stu-id="9ba24-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="9ba24-121">Código-fonte completo do aplicativo auxiliar de IP</span><span class="sxs-lookup"><span data-stu-id="9ba24-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="9ba24-122">Exemplos do auxiliar de IP avançado</span><span class="sxs-lookup"><span data-stu-id="9ba24-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="9ba24-123">Vários exemplos mais avançados de auxiliares de IP estão incluídos no Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9ba24-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ba24-124">Por padrão, o código-fonte de exemplo do auxiliar de IP é instalado pelo SDK do Windows lançado para o Windows 7 no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="9ba24-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="9ba24-125">*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ IPHelp*</span><span class="sxs-lookup"><span data-stu-id="9ba24-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="9ba24-126">Os exemplos mais avançados listados abaixo são encontrados nos seguintes diretórios:</span><span class="sxs-lookup"><span data-stu-id="9ba24-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="9ba24-127">EnableRouter</span><span class="sxs-lookup"><span data-stu-id="9ba24-127">EnableRouter</span></span>

    <span data-ttu-id="9ba24-128">Esse diretório contém um exemplo que demonstra como usar as funções auxiliares de IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) e [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) para habilitar e desabilitar o encaminhamento de IPv4 no computador local.</span><span class="sxs-lookup"><span data-stu-id="9ba24-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="9ba24-129">iparp</span><span class="sxs-lookup"><span data-stu-id="9ba24-129">iparp</span></span>

    <span data-ttu-id="9ba24-130">Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para exibir e manipular entradas na tabela ARP IPv4 no computador local.</span><span class="sxs-lookup"><span data-stu-id="9ba24-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="9ba24-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="9ba24-131">ipchange</span></span>

    <span data-ttu-id="9ba24-132">Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para alterar programaticamente um endereço IP para um adaptador de rede específico em seu computador.</span><span class="sxs-lookup"><span data-stu-id="9ba24-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="9ba24-133">Este programa também demonstra como recuperar informações de configuração de IP do adaptador de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="9ba24-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="9ba24-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="9ba24-134">IPConfig</span></span>

    <span data-ttu-id="9ba24-135">Esse diretório contém um programa de exemplo que demonstra como recuperar programaticamente as informações de configuração de IPv4 semelhantes ao utilitário IPCONFIG.EXE.</span><span class="sxs-lookup"><span data-stu-id="9ba24-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="9ba24-136">Ele demonstra como usar as funções [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) e [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="9ba24-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="9ba24-137">Observe que a função **GetAdaptersInfo** recupera apenas informações de IPv4.</span><span class="sxs-lookup"><span data-stu-id="9ba24-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="9ba24-138">IPRenew</span><span class="sxs-lookup"><span data-stu-id="9ba24-138">IPRenew</span></span>

    <span data-ttu-id="9ba24-139">Esse diretório contém um programa de exemplo que demonstra como lançar e renovar programaticamente os endereços IPv4 obtidos por meio do DHCP.</span><span class="sxs-lookup"><span data-stu-id="9ba24-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="9ba24-140">Este programa também demonstra como recuperar informações de configuração de adaptador de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="9ba24-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="9ba24-141">IPRoute</span><span class="sxs-lookup"><span data-stu-id="9ba24-141">IPRoute</span></span>

    <span data-ttu-id="9ba24-142">Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para manipular a tabela de roteamento IPv4.</span><span class="sxs-lookup"><span data-stu-id="9ba24-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="9ba24-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="9ba24-143">ipstat</span></span>

    <span data-ttu-id="9ba24-144">Esse diretório contém um programa de exemplo que demonstra como usar as funções auxiliares de IP para mostrar conexões IPv4 para um protocolo.</span><span class="sxs-lookup"><span data-stu-id="9ba24-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="9ba24-145">Por padrão, as estatísticas são mostradas para IP, ICMP, TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="9ba24-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="9ba24-146">NetInfo</span><span class="sxs-lookup"><span data-stu-id="9ba24-146">Netinfo</span></span>

    <span data-ttu-id="9ba24-147">Esse diretório contém um programa de exemplo que demonstra como usar as novas APIs auxiliares de IP introduzidas no Windows Vista e versões posteriores para exibir/alterar informações de endereço e de interface para IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="9ba24-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



