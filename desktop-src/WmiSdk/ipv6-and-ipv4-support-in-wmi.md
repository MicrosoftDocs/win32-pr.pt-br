---
description: O provedor de rotas IP WMI e as classes de rede fornecem dados para endereços IPv4. A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6.
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: Suporte a IPv6 e IPv4 no WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761792"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="5aa2c-104">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="5aa2c-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="5aa2c-105">O [provedor de rotas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e as classes de rede fornecem dados para endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="5aa2c-106">A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="5aa2c-107">Dados IP do WMI</span><span class="sxs-lookup"><span data-stu-id="5aa2c-107">WMI IP Data</span></span>

<span data-ttu-id="5aa2c-108">As classes a seguir fornecem apenas dados IPv4:</span><span class="sxs-lookup"><span data-stu-id="5aa2c-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="5aa2c-109">**\_IP4RouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="5aa2c-110">**\_IP4PersistedRouteTable Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="5aa2c-111">**\_IP4RouteTableEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="5aa2c-112">**\_ActiveRoute Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="5aa2c-113">**\_Adaptador Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="5aa2c-114">As classes a seguir fornecem dados para IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="5aa2c-115">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="5aa2c-116">A propriedade **IpAddess** contém o endereço IPv6 do computador em uma rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="5aa2c-117">**\_PingStatus Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa2c-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="5aa2c-118">[**Win32 \_ O PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) pode retornar dados para endereços IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="5aa2c-119">Conexões IPv4 e IPv6 com o WMI</span><span class="sxs-lookup"><span data-stu-id="5aa2c-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="5aa2c-120">Ao se conectar a um namespace WMI em um computador remoto, o computador de destino deve estar executando o mesmo software IP que o computador que está se conectando.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="5aa2c-121">Por exemplo, um computador que executa o IPv4 não pode se conectar a um computador executando IPv6, mesmo que a conexão seja tentada usando um nome de computador na chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)ou usando a `winmgmts` conexão do moniker.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="5aa2c-122">O inverso também é verdadeiro: um computador executando somente o IPv6 não pode se conectar a um computador que executa apenas o IPv4.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="5aa2c-123">Se o computador de destino estiver executando o IPv4 e o IPv6, uma conexão poderá ser feita de um computador que executa o software IP.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="5aa2c-124">Um nome de computador ou um endereço IP no formato IPv4 ou IPv6 pode ser fornecido na conexão com um namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="5aa2c-125">Um computador que executa IPv4 e IPv6 e se conecta a um computador de destino que executa somente IPv4 ou apenas IPv6 deve fornecer um endereço IP no formato apropriado para o software IP do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5aa2c-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa2c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5aa2c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa2c-127">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="5aa2c-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
