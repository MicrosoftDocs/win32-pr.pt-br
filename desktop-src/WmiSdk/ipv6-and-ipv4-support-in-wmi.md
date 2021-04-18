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
# <a name="ipv6-and-ipv4-support-in-wmi"></a>Suporte a IPv6 e IPv4 no WMI

O [provedor de rotas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e as classes de rede fornecem dados para endereços IPv4. A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6.

## <a name="wmi-ip-data"></a>Dados IP do WMI

As classes a seguir fornecem apenas dados IPv4:

-   [**\_IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [**\_IP4PersistedRouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [**\_IP4RouteTableEvent Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [**\_ActiveRoute Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [**\_Adaptador Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

As classes a seguir fornecem dados para IPv4 e IPv6.

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    A propriedade **IpAddess** contém o endereço IPv6 do computador em uma rede IPv6.

-   [**\_PingStatus Win32**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    [**Win32 \_ O PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) pode retornar dados para endereços IPv4 ou IPv6.

## <a name="ipv4-and-ipv6-connections-to-wmi"></a>Conexões IPv4 e IPv6 com o WMI

Ao se conectar a um namespace WMI em um computador remoto, o computador de destino deve estar executando o mesmo software IP que o computador que está se conectando. Por exemplo, um computador que executa o IPv4 não pode se conectar a um computador executando IPv6, mesmo que a conexão seja tentada usando um nome de computador na chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md)ou usando a `winmgmts` conexão do moniker. O inverso também é verdadeiro: um computador executando somente o IPv6 não pode se conectar a um computador que executa apenas o IPv4.

Se o computador de destino estiver executando o IPv4 e o IPv6, uma conexão poderá ser feita de um computador que executa o software IP. Um nome de computador ou um endereço IP no formato IPv4 ou IPv6 pode ser fornecido na conexão com um namespace WMI.

Um computador que executa IPv4 e IPv6 e se conecta a um computador de destino que executa somente IPv4 ou apenas IPv6 deve fornecer um endereço IP no formato apropriado para o software IP do computador de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
