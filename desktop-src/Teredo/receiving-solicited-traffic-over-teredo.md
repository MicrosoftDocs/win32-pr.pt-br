---
title: Recebendo tráfego solicitado por Teredo
description: Muitos aplicativos, como o Microsoft Internet Explorer e o Microsoft Outlook, só iniciam conexões com a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104499174"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Recebendo tráfego solicitado por Teredo

Muitos aplicativos, como o Microsoft Internet Explorer e o Microsoft Outlook, só iniciam conexões com a Internet. Para esses aplicativos, o [Teredo](about-teredo.md) pode fornecer conectividade direta sobre o IPv6 na ausência de outras interfaces IPv6. Além disso, o tráfego solicitado pode ser recebido pela interface teredo nas plataformas anteriores do Microsoft Windows XP com Service Pack 2 (SP2) e Windows Server 2003.

A documentação a seguir explica como esses aplicativos obtêm conectividade e as circunstâncias sob as quais o Teredo é usado.

## <a name="obtaining-a-destination-address"></a>Obtendo um endereço de destino

Um aplicativo tenta obter o endereço de destino usando vários métodos, como DNS (sistema de nomes de domínio) ou PNRP (Peer Name Resolution Protocol). É possível que o aplicativo obtenha vários endereços IP IPv4 e IPv6 usando esses métodos. As APIs típicas usadas para obter endereços IP incluem a API do Windows XP [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e a nova API do Windows Vista [**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Por exemplo, usar a API GetAddrInfo com o *parâmetro \_ Family da família ia* definido \_ como AF INET6 como a dica addrinfo/Protocol permite ao usuário consultar servidores DNS para endereços IPv6 especificamente. A API [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) com o tipo DNS \_ Type \_ aaaa também pode ser usada para consultar os servidores DNS para registros AAAA.

## <a name="establishing-a-connection"></a>Estabelecer uma conexão

Uma conexão estabelecida com o Teredo é descrita como ' direta ' porque ela é tratada como qualquer outra conexão IPv6. A programação de um aplicativo não exige uma consideração especial para ser capaz de utilizar a interface teredo. Quando uma conexão é estabelecida entre as interfaces Teredo, um roteador de retransmissão, típico de 6to4 e outras interfaces nativas, não é necessário. No entanto, o Teredo foi projetado como uma tecnologia de transição de último recurso para conectividade IPv6.

> [!Note]  
> O Teredo não será utilizado se o nome de host fornecido resolver somente para endereços IPv4.

 

Quando um aplicativo tenta se conectar a um destino usando endereços IPv6, ocorrerá o seguinte:

-   O aplicativo obtém uma lista de endereços IPv6 chamando a API [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) . A pilha do Windows Vista retorna uma lista de todas as interfaces com base na ordem de classificação especificada no [RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Como resultado, as interfaces IPv6 IPv6 e 6to4 serão listadas antes da interface teredo. No entanto, quando a conectividade IPv6 ou 6to4 nativa não estiver disponível, o Teredo será a única interface compatível com IPv6 listada.

    É importante lembrar-se de que um aplicativo pode usar qualquer interface fornecida pela pilha do Windows Vista, no entanto, a ordenação da lista de interface retornada resultará na tentativa do Teredo pela última vez.

-   Antes que o Windows Vista tente uma conexão pela interface teredo, o sistema operacional garante que o endereço IPv6 tenha estabilizado. Isso é feito automaticamente para conexões de saída e não é uma consideração crucial para um aplicativo. Caso o aplicativo seja necessário para garantir a estabilidade do endereço, a API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) pode ser chamada para garantir que o endereço Teredo seja estável.

-   Uma interface teredo tentará se conectar a outra interface teredo no destino. Se uma interface teredo não estiver presente, uma conexão será estabelecida com um endereço de destino nativo ou 6to4 por meio de uma retransmissão específica do host.

Também é possível que os aplicativos que iniciam conexões com a Internet recebam tráfego não solicitado. Para obter mais detalhes, consulte [recebendo tráfego não solicitado por Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Usando a API WSAConnectByName

Ao chamar a API WSAConnectByName, é possível que um aplicativo se conecte a um nome de destino em vez de especificar o endereço IP exato. A pilha do Windows Vista prefere IPv6 sobre IPv4 e, como resultado, todas as tentativas de conexão serão feitas em endereços IPv6 primeiro.

Chamar a API WSAConnectByName classificará todos os endereços IP de destino obtidos na seguinte ordem:

-   Endereço IPv6 nativo
-   Endereço IP 6to4
-   Endereço IPv4
-   Endereço Teredo

Depois que os endereços de destino são classificados internamente, uma conexão com o destino é tentada com base na melhor rota disponível no host local para o endereço de destino. Conforme indicado pela ordem dos endereços classificados, se o nome de destino for resolvido para um endereço IPv4 e Teredo, o endereço IPv4 será usado para estabelecer a conexão.

A API do WSAConnectByName funciona internamente para encontrar a melhor correspondência entre os endereços. Essa tentativa é baseada nas rotas disponíveis no host local e nos endereços de destino.

Devido à ausência atual de retransmissões Teredo na Internet, é improvável que as conexões com endereços IPv6 nativos tenham sucesso na interface teredo. Se WSAConnectByName for chamado, o Windows Vista não emitirá consultas AAAA quando o Teredo for a única interface compatível com IPv6 disponível. Isso garante que os endereços IPv6 nativos não sejam obtidos como destino e que as conexões sejam tentadas por IPv4, o que tem a maior chance de sucesso. Para obter endereços IPv6 quando Teredo é a única interface compatível com IPv6, um aplicativo deve usar explicitamente a API do DnsQuery para registros AAAA.

 

 