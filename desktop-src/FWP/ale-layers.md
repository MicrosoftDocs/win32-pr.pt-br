---
title: Camadas ALE
description: A ALE (aplicação de camada de aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293922"
---
# <a name="ale-layers"></a>Camadas ALE

A ALE (aplicação da camada de aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes. Todas as camadas do mecanismo de filtragem da WFP (plataforma de filtragem do Windows), incluindo a EPA, são descritas em [**identificadores de camada**](management-filtering-layer-identifiers-.md)de filtragem. Este tópico contém uma descrição mais detalhada das camadas de filtragem que fazem parte da EPA.

## <a name="resource_assignment"></a>atribuição de recursos \_

Um filtro na camada [**de \_ atribuição de recurso Ale da camada FWPM \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido para operações de ligação de rede, explícita ou implícita.

Se um filtro nessa camada for correspondido para autorizar a criação de soquetes brutos, o sinalizador de condição fwp será definido como sinalizador de [**\_ ponto de \_ \_ \_ \_ extremidade bruto**](filtering-condition-flags-.md) .

Se um filtro nessa camada for correspondido para autorizar o recebimento do modo promíscuo, o campo de [**\_ \_ \_ \_ modo promíscuo de Ale da condição fwp**](filtering-condition-identifiers-.md) será definido como sio \_ RCVALL. Para obter uma descrição de SIO \_ RCVALL, consulte [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Essa é a única camada em que o modo promíscuo pode ser filtrado.

 

Se nenhuma porta for especificada durante a **ligação ()**, ou seja, a porta for definida como 0 (zero), a pilha TCP/IP selecionará uma porta do intervalo de portas dinâmicas (19152 – 65535). A porta selecionada será classificada nesta camada junto com o [**sinalizador de condição fwp é um sinalizador de \_ \_ \_ \_ \_ ligação curinga**](filtering-condition-flags-.md) .

Se o endereço local não for especificado na chamada [**BIND ()**](/windows/desktop/api/winsock/nf-winsock-bind) , o campo endereço local será definido como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

## <a name="auth_listen"></a>Escuta de autenticação \_

Um filtro na camada [**\_ \_ \_ \_ \_ V {4 \| 6} da autenticação Ale da camada FWPM**](management-filtering-layer-identifiers-.md) é correspondido para chamadas TCP [**() de escuta**](/windows/desktop/api/winsock2/nf-winsock2-listen) .

## <a name="auth_recv_accept"></a>\_aceitação de recv de autenticação \_

Um filtro na camada de [**FWPM de \_ autenticação Ale de camada de \_ \_ \_ recepção \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido para chamadas de [**aceitação TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , para os primeiros pacotes UDP (unicast) de uma tupla de endereço/porta remoto exclusiva e para as primeiras mensagens ICMP de não erro de entrada (unicast) com um tipo de ICMP, código e ID exclusivos.

> [!Note]  
> Protocolos que não são TCP ou ICMP são tratados como UDP.

 

Os pacotes TCP recebidos por soquetes brutos são tratados de forma semelhante ao tráfego UDP. Ou seja, somente o primeiro TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre soquetes brutos serão filtrados.

## <a name="auth_connect"></a>conexão de autenticação \_

Um filtro na camada [**\_ \_ \_ \_ \_ V {4 \| 6} da autenticação Ale da camada FWPM**](management-filtering-layer-identifiers-.md) é correspondido para chamadas de [**conexão TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , para os primeiros pacotes UDP enviados a uma tupla de porta e um endereço remoto exclusivo, e para as primeiras mensagens ICMP de não erro de saída com um tipo ICMP, código e ID exclusivos.

> [!Note]  
> Protocolos que não são TCP ou ICMP são tratados como UDP.

 

Os pacotes TCP enviados por soquetes brutos são tratados de forma semelhante ao tráfego UDP. Ou seja, somente o primeiro TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sobre soquetes brutos serão filtrados.

## <a name="flow_established"></a>FLUXO \_ estabelecido

Um filtro no [**\_ fluxo Ale da camada de FWPM \_ estabeleceu uma camada \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) correspondente depois que um handshake de três vias TCP for concluído com êxito. Para o tráfego não TCP, o filtro é correspondido imediatamente após os filtros das camadas de **\_ \_ aceitação de recv de autenticação** ou de **\_ conexão de autenticação** serem correspondidos.

Um filtro nesta camada não deve retornar o bloco ou a permissão.

Essa camada é usada por drivers de texto explicativo para acompanhar o estado de conexão, descrito em detalhes na documentação do [Kit de driver do Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="resource_release"></a>versão do recurso \_

Um filtro na camada [**do \_ recurso Ale da camada FWPM da \_ \_ \_ versão \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido depois que os recursos alocados por meio da **\_ atribuição de recursos** foram liberados.

## <a name="endpoint_closure"></a>encerramento do ponto de extremidade \_

Um filtro na camada de [**fechamento de ponto de extremidade da camada FWPM do \_ \_ \_ \_ encerramento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) é correspondido quando um fluxo TCP conectado ou um ponto de extremidade de soquetes UDP é fechado.

## <a name="connect_redirect"></a>redirecionamento de conexão \_

Um filtro na camada [**\_ \_ \_ \_ redirecionamento Ale Connect \_ V {4 \| 6} da camada FWPM**](management-filtering-layer-identifiers-.md) permite a modificação de endereços e portas remotos. A conexão de saída será redirecionada pela duração dessa conexão.

## <a name="bind_redirect"></a>redirecionamento de associação \_

Um filtro na camada [**\_ \_ \_ \_ redirecionamento Ale BIND \_ V {4 \| 6} da camada FWPM**](management-filtering-layer-identifiers-.md) permite a modificação do endereço local e das portas do soquete subjacente. O soquete local será redirecionado durante o tempo de vida do soquete

## <a name="ale-discard-layers"></a>Camadas de descarte ALE

Para cada uma das camadas ALE descritas acima, o mecanismo de filtragem contém uma camada de descarte correspondente. As camadas de descarte ALE são usadas por textos explicativos para fins de log. Os pacotes e as indicações que foram descartadas em uma das camadas de filtragem ALE são indicados para a camada de descarte ALE correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação da camada de aplicativo (EPA)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtragem de estado de ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego de difusão/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de fluxo ALE](ale-flow-customization.md)
</dt> <dt>

[Fluxos de pacotes TCP](tcp-packet-flows.md)
</dt> <dt>

[Fluxos de pacotes UDP](udp-packet-flows.md)
</dt> <dt>

[Funções do Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Filtrando sinalizadores de condição**](filtering-condition-flags-.md)
</dt> <dt>

[**Condições de filtragem disponíveis em cada camada de filtragem**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 