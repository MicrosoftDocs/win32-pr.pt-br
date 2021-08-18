---
title: Recebendo tráfego solicitado em Teredo
description: Muitos aplicativos, como o Microsoft Internet Explorer e o Microsoft Outlook iniciam conexões com a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f003755f49d04113108f83c8d3eff67084364ad6dfcf8e9f40cf1bf7e142e0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001674"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Recebendo tráfego solicitado em Teredo

Muitos aplicativos, como o Microsoft Internet Explorer e o Microsoft Outlook iniciam conexões com a Internet. Para esses aplicativos, [o Teredo](about-teredo.md) pode fornecer conectividade contínua sobre IPv6 na ausência de outras interfaces IPv6. Além disso, o tráfego solicitado pode ser recebido pela Interface teredo nas plataformas Anteriores do Microsoft Windows XP com Service Pack 2 (SP2) e Windows Server 2003.

A documentação a seguir explica como esses aplicativos atingem conectividade e as circunstâncias em que o Teredo é usado.

## <a name="obtaining-a-destination-address"></a>Obtendo um endereço de destino

Um aplicativo tenta obter o endereço de destino usando vários métodos, como DNS (Sistema de Nomes de Domínio) ou PROTOCOLO PNRP. É possível que o aplicativo obtenha vários endereços IP IPv4 e IPv6 usando esses métodos. As APIs típicas usadas para obter endereços IP incluem o [**getHostByName**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) da API Windows XP e o novo [**getAddrInfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)da API Windows Vista. Por exemplo, o uso da API GetAddrInfo com o parâmetro de família *ai \_* definido como AF INET6, pois a dica addrinfo/protocol permite que o usuário consulte servidores DNS para \_ endereços IPv6 especificamente. A API [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) com o tipo DNS TYPE AAAA também pode ser usada para consultar os servidores DNS para \_ \_ registros AAAA.

## <a name="establishing-a-connection"></a>Estabelecer uma conexão

Uma conexão estabelecida com o Teredo é descrita como "perfeita" porque é tratada como qualquer outra conexão IPv6. A programação de um aplicativo não requer consideração especial para ser capaz de utilizar a interface Teredo. Quando uma conexão é estabelecida entre interfaces Teredo, um roteador de retransmissão, típico de 6to4 e outras interfaces nativas, não é necessário. No entanto, o Teredo foi projetado como uma tecnologia de transição de último recurso para conectividade IPv6.

> [!Note]  
> Teredo não será utilizado se o nome do host fornecido for resolvido apenas para endereços IPv4.

 

Quando um aplicativo tentar se conectar a um destino usando endereços IPv6, ocorrerá o seguinte:

-   O aplicativo obtém uma lista de endereços IPv6 chamando a API [**GetAdaptersAddresses.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) A Windows vista retorna uma lista de todas as interfaces com base na ordem de classificação especificada no [RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Como resultado, as interfaces IPv6 e 6to4 IPv6 serão listadas antes da interface Teredo. No entanto, quando a conectividade IPv6 ou 6to4 nativa não estiver disponível, o Teredo será a única interface com capacidade para IPv6 listada.

    É importante lembrar que um aplicativo pode usar qualquer interface fornecida pela pilha Windows Vista, no entanto, a ordenação da lista de interfaces retornada geralmente resultará na última tentativa do Teredo.

-   Antes Windows vista tenta uma conexão pela interface Teredo, o sistema operacional garante que o endereço IPv6 tenha estabilizado. Isso é feito automaticamente para conexões de saída e não é uma consideração crucial para um aplicativo. Caso o aplicativo seja necessário para garantir a estabilidade do endereço, a API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) poderá ser chamada para garantir que o endereço Teredo seja estável.

-   Uma interface Teredo tentará se conectar a outra interface Teredo no destino. Se uma interface Teredo não estiver presente, uma conexão será estabelecida com um endereço de destino nativo ou 6to4 por meio de uma retransmissão específica do host.

Também é possível que os aplicativos que iniciam conexões com a Internet recebam tráfego não solicitado. Para obter mais detalhes, [consulte Recebendo tráfego não solicitado em Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Usando a API WSAConnectByName

Ao chamar a API WSAConnectByName, é possível que um aplicativo se conecte a um nome de destino em vez de especificar o endereço IP exato. A Windows Vista prefere IPv6 em vez de IPv4 e, como resultado, todas as tentativas de conexão serão feitas em endereços IPv6 primeiro.

Chamar a API WSAConnectByName classificará todos os endereços IP de destino obtidos na seguinte ordem:

-   Endereço IPv6 nativo
-   6to4 ENDEREÇO IP
-   Endereço IPv4
-   Endereço teredo

Depois que os endereços de destino são classificação internamente, uma conexão com o destino é tentada com base na melhor rota disponível no host local para o endereço de destino. Conforme indicado pela ordem dos endereços classificação, se o nome de destino for resolvido para um endereço IPv4 e Teredo, o endereço IPv4 será usado para estabelecer a conexão.

A API WSAConnectByName funciona internamente para encontrar a melhor combinação entre endereços. Essa tentativa se baseia nas rotas disponíveis no host local e nos endereços de destino.

Devido à ausência atual de retransmissão teredo na Internet, é improvável que as conexões com endereços IPv6 nativos sejam bem-sucedidas na interface Teredo. Se WSAConnectByName for chamado, Windows Vista não emitirá consultas AAAA quando Teredo for a única interface com capacidade para IPv6 disponível. Isso garante que os endereços IPv6 nativos não sejam obtidos como um destino e que as conexões sejam tentadas por IPv4, que tem a maior chance de sucesso. Para obter endereços IPv6 quando Teredo é a única interface com capacidade para IPv6, um aplicativo deve usar explicitamente a API DnsQuery para registros AAAA.

 

 