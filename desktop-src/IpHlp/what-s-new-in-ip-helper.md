---
description: Novidades no Auxiliar de IP
ms.assetid: fa9d72d0-2f9c-433d-b05a-8423664b2e3e
title: Novidades no Auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3141797e96442f34a94c2d2afc37585ce6dbc944e7fb35cf9b4602afa042c95a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897616"
---
# <a name="whats-new-in-ip-helper"></a>Novidades no Auxiliar de IP

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Os recursos a seguir foram adicionados às APIs auxiliares de IP Windows 8 e Windows Server 2012.

Uma função que recupera estimativas de largura de banda históricas para uma conexão de rede. Para obter mais informações, consulte:

-   [**GetIpNetworkConnectionBandwidthEstimates**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetworkconnectionbandwidthestimates)

Uma estrutura que contém informações sobre as estimativas de largura de banda disponíveis e a variação associada, conforme determinado pela pilha TCP/IP. Para obter mais informações, consulte:

-   [**INFORMAÇÕES DE LARGURA DE \_ BANDA NL \_**](/windows/desktop/api/Nldef/ns-nldef-nl_bandwidth_information)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Os recursos a seguir foram adicionados às APIs auxiliares de IP no Windows 7 e Windows Server 2008 R2.

Funções que convertem um endereço Ethernet entre um formato binário e um formato de cadeia de caracteres para o endereço MAC Ethernet. Para obter mais informações, consulte:

-   [**RtlEthernetAddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetaddresstostringa)
-   [**RtlEthernetStringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlethernetstringtoaddressa)

## <a name="windows-server-2008-and-windows-vista-sp1"></a>Windows Server 2008 e Windows Vista SP1

As funções a seguir foram adicionadas às APIs auxiliares de IP no Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).

Uma função que funciona com IPv4 e o PROTOCOLO ICMP. Para obter mais informações, consulte:

-   [**IcmpSendEcho2Ex**](/windows/desktop/api/Icmpapi/nf-icmpapi-icmpsendecho2ex)

## <a name="windows-vista"></a>Windows Vista

Os grupos de funções a seguir foram adicionados às APIs auxiliares de IP no Windows Vista e posterior.

Funções que funcionam com IPv6 e IPv4 para conversão de interface. Para obter mais informações, consulte:

-   [**ConvertInterfaceAliasToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacealiastoluid)
-   [**ConvertInterfaceGuidToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceguidtoluid)
-   [**ConvertInterfaceIndexToLuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceindextoluid)
-   [**ConvertInterfaceLuidToGuid**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoguid)
-   [**ConvertInterfaceLuidToIndex**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtoindex)
-   [**ConvertInterfaceLuidToNameA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamea)
-   [**ConvertInterfaceLuidToNameW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfaceluidtonamew)
-   [**ConvertInterfaceNameToLuidA**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluida)
-   [**ConvertInterfaceNameToLuidW**](/windows/desktop/api/Netioapi/nf-netioapi-convertinterfacenametoluidw)
-   [**se \_ indextoname**](/windows/desktop/api/Netioapi/nf-netioapi-if_indextoname)
-   [**se \_ nametoindex**](/windows/desktop/api/Netioapi/nf-netioapi-if_nametoindex)

Funções que funcionam com IPv6 e IPv4 para gerenciamento de interface. Para obter mais informações, consulte:

-   [**GetIfEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getifentry2)
-   [**GetIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getifstacktable)
-   [**GetIfTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2)
-   [**GetIfTable2Ex**](/windows/desktop/api/Netioapi/nf-netioapi-getiftable2ex)
-   [**GetInvertedIfStackTable**](/windows/desktop/api/Netioapi/nf-netioapi-getinvertedifstacktable)
-   [**GetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfaceentry)
-   [**GetIpInterfaceTable**](/windows/desktop/api/Netioapi/nf-netioapi-getipinterfacetable)
-   [**InitializeIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipinterfaceentry)
-   [**SetIpInterfaceEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setipinterfaceentry)

Funções que funcionam com IPv6 e IPv4 para gerenciamento de endereços IP. Para obter mais informações, consulte:

-   [**CreateAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createanycastipaddressentry)
-   [**CreateUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-createunicastipaddressentry)
-   [**DeleteAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteanycastipaddressentry)
-   [**DeleteUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-deleteunicastipaddressentry)
-   [**GetAnycastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddressentry)
-   [**GetAnycastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getanycastipaddresstable)
-   [**GetMulticastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddressentry)
-   [**GetMulticastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getmulticastipaddresstable)
-   [**GetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddressentry)
-   [**GetUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-getunicastipaddresstable)
-   [**InitializeUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeunicastipaddressentry)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)
-   [**SetUnicastIpAddressEntry**](/windows/desktop/api/Netioapi/nf-netioapi-setunicastipaddressentry)

Uma função que funciona com IPv6 e IPv4 para gerenciamento de memória de tabela IP. Para obter mais informações, consulte:

-   [**FreeMibTable**](/windows/desktop/api/Netioapi/nf-netioapi-freemibtable)

Funções que funcionam com IPv6 e IPv4 para gerenciamento de endereços de vizinho IP. Para obter mais informações, consulte:

-   [**CreateIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipnetentry2)
-   [**DeleteIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipnetentry2)
-   [**FlushIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-flushipnettable2)
-   [**GetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnetentry2)
-   [**GetIpNetTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipnettable2)
-   [**ResolveIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-resolveipnetentry2)
-   [**ResolveNeighbor**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-resolveneighbor)
-   [**SetIpNetEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipnetentry2)

Funções que funcionam com IPv6 e IPv4 para gerenciamento de caminho IP. Para obter mais informações, consulte:

-   [**FlushIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-flushippathtable)
-   [**GetIpPathEntry**](/windows/desktop/api/Netioapi/nf-netioapi-getippathentry)
-   [**GetIpPathTable**](/windows/desktop/api/Netioapi/nf-netioapi-getippathtable)

Funções que funcionam com IPv6 e IPv4 para gerenciamento de rotas de IP. Para obter mais informações, consulte:

-   [**CreateIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-createipforwardentry2)
-   [**DeleteIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-deleteipforwardentry2)
-   [**GetBestRoute2**](/windows/desktop/api/Netioapi/nf-netioapi-getbestroute2)
-   [**GetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardentry2)
-   [**GetIpForwardTable2**](/windows/desktop/api/Netioapi/nf-netioapi-getipforwardtable2)
-   [**InitializeIpForwardEntry**](/windows/desktop/api/Netioapi/nf-netioapi-initializeipforwardentry)
-   [**SetIpForwardEntry2**](/windows/desktop/api/Netioapi/nf-netioapi-setipforwardentry2)
-   [**SetIpStatisticsEx**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatisticsex)

Funções que funcionam com IPv6 e IPv4 para notificação. Para obter mais informações, consulte:

-   [**CancelMibChangeNotify2**](/windows/desktop/api/Netioapi/nf-netioapi-cancelmibchangenotify2)
-   [**NotifyIpInterfaceChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyipinterfacechange)
-   [**NotifyRouteChange2**](/windows/desktop/api/Netioapi/nf-netioapi-notifyroutechange2)
-   [**NotifyUnicastIpAddressChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyunicastipaddresschange)

Funções de utilitário que funcionam com endereços IP. Para obter mais informações, consulte:

-   [**ConvertIpv4MaskToLength**](/windows/desktop/api/Netioapi/nf-netioapi-convertipv4masktolength)
-   [**ConvertLengthToIpv4Mask**](/windows/desktop/api/Netioapi/nf-netioapi-convertlengthtoipv4mask)
-   [**CreateSortedAddressPairs**](/windows/desktop/api/Netioapi/nf-netioapi-createsortedaddresspairs)
-   [**ParseNetworkString**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-parsenetworkstring)

Funções que funcionam com protocolo TCP e UDP para recuperar a tabela de conexões TCP IPv6 ou IPv4 ou UDP. Para obter mais informações, consulte:

-   [**GetTcp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table)
-   [**GetTcp6Table2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcp6table2)
-   [**GetTcpTable2**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable2)
-   [**GetUdp6Table**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudp6table)

Funções que funcionam com o protocolo TCP para recuperar estatísticas TCP estendidas em uma conexão. Para obter mais informações, consulte:

-   [**GetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcp6connectionestats)
-   [**GetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getpertcpconnectionestats)
-   [**SetPerTcp6ConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcp6connectionestats)
-   [**SetPerTcpConnectionEStats**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setpertcpconnectionestats)

Novas funções que funcionam para o gerenciamento de clientes teredo IPv6. Para obter mais informações, consulte:

-   [**GetTeredoPort**](/windows/desktop/api/Netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/Netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/Netioapi/nf-netioapi-notifystableunicastipaddresstable)

Funções de utilitário que fornecem conversões entre endereços IP e representações de cadeia de caracteres de endereços IP. Para obter mais informações, consulte:

-   [**RtlIpv4AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa)
-   [**RtlIpv4AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw)
-   [**RtlIpv4StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa)
-   [**RtlIpv4StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw)
-   [**RtlIpv6AddressToString**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa)
-   [**RtlIpv6AddressToStringEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)
-   [**RtlIpv6StringToAddress**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)
-   [**RtlIpv6StringToAddressEx**](/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw)

Funções que fornecem reservas persistentes para um bloco consecutivo de portas TCP ou UDP no computador local. Para obter mais informações, consulte:

-   [**CreatePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)
-   [**CreatePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createpersistentudpportreservation)
-   [**DeletePersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)
-   [**DeletePersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)
-   [**LookupPersistentTcpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)
-   [**LookupPersistentUdpPortReservation**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

## <a name="windows-server-2003"></a>Windows Server 2003

As seguintes funções foram adicionadas às APIs auxiliares de IP no Windows Server 2003 e posterior:

-   [**CancelSecurityHealthChangeNotify**](/previous-versions/windows/desktop/legacy/bb442512(v=vs.85))
-   [**NotifySecurityHealthChange**](/previous-versions/windows/desktop/legacy/bb451761(v=vs.85))

## <a name="windows-xp-sp2"></a>Windows XP SP2

As seguintes funções foram adicionadas às APIs auxiliares de IP no Windows XP com o Service Pack 2 (SP2) e posterior:

-   [**GetOwnerModuleFromTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcpentry)
-   [**GetOwnerModuleFromTcp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry)
-   [**GetOwnerModuleFromUdpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudpentry)
-   [**GetOwnerModuleFromUdp6Entry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getownermodulefromudp6entry)

 

 
