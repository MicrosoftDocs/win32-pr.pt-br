---
title: Camadas ALE
description: A ALE (Imposição de Camada de Aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901006"
---
# <a name="ale-layers"></a>Camadas ALE

A ALE (Imposição de Camada de Aplicativo) consiste em várias camadas de filtragem e muitas camadas de descarte correspondentes. Todas as camadas do mecanismo de filtragem Windows WFP (Plataforma de Filtragem de Dados), incluindo a ALE, são descritas em Identificadores de Camada [**de Filtragem**](management-filtering-layer-identifiers-.md). Este tópico contém uma descrição mais detalhada das camadas de filtragem que fazem parte do ALE.

## <a name="resource_assignment"></a>ATRIBUIÇÃO DE \_ RECURSOS

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ \| V{4 6}**](management-filtering-layer-identifiers-.md) é corresponder a operações de vinculação de rede, explícitas ou implícitas.

Se um filtro nessa camada for corresponder para autorizar a criação de soquete bruto, o sinalizador [**FWP \_ CONDITION IS RAW \_ \_ \_ \_ ENDPOINT**](filtering-condition-flags-.md) será definido.

Se um filtro nessa camada for corresponder para autorizar o recebimento do modo promiscuo, o campo [**FWP \_ CONDITION \_ ALE \_ PROMISCUOUS \_ MODE**](filtering-condition-identifiers-.md) será definido como SIO \_ RC LTDA. Para ver uma descrição de SIO \_ RC LTDA, [**consulte WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Essa é a única camada em que o modo promiscuo pode ser filtrado.

 

Se nenhuma porta for especificada durante **bind(),** ou seja, a porta for definida como 0 (zero), a pilha TCP/IP selecionará uma porta do intervalo de portas dinâmico (19152–65535). A porta selecionada será classificada nessa camada junto com o sinalizador [**FWP \_ CONDITION \_ IS \_ \_ WILDCARD \_ BIND.**](filtering-condition-flags-.md)

Se o endereço local não for especificado na chamada [**bind(),**](/windows/desktop/api/winsock/nf-winsock-bind) o campo de endereço local será definido como [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)

## <a name="auth_listen"></a>AUTH \_ LISTEN

Um filtro na camada [**FWPM \_ LAYER \_ \_ ALE AUTH \_ LISTEN \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) é corresponder a chamadas TCP [**listen().**](/windows/desktop/api/winsock2/nf-winsock2-listen)

## <a name="auth_recv_accept"></a>ACEITAR \_ RECV DE AUTH \_

Um filtro na camada RECV ACCEPT [**V{4 6} do FWPM \_ LAYER \_ \_ ALE AUTH \_ ACEITA \_ \_ \| V{4 6}**](management-filtering-layer-identifiers-.md) é corresponder a chamadas TCP [**accept(),**](/windows/desktop/api/winsock2/nf-winsock2-accept) para os primeiros pacotes UDP (unicast) de um endereço remoto/tupla de porta exclusivo e para as primeiras mensagens ICMP sem erro de entrada (unicast) com um tipo, código e ID icMP exclusivos.

> [!Note]  
> Protocolos que não são TCP ou ICMP são tratados como UDP.

 

Os pacotes TCP recebidos por soquetes brutos são tratados da mesma forma que o tráfego UDP. Ou seja, somente o primeiro TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) em soquetes brutos serão filtrados.

## <a name="auth_connect"></a>AUTH \_ CONNECT

Um filtro na camada [**FWPM \_ LAYER \_ \_ ALE AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) é corresponder a chamadas TCP [**connect(),**](/windows/desktop/api/winsock2/nf-winsock2-connect) para os primeiros pacotes UDP enviados para um endereço remoto exclusivo e uma tupla de porta e para as primeiras mensagens ICMP sem erro de saída com um tipo, código e ID icMP exclusivos.

> [!Note]  
> Protocolos que não são TCP ou ICMP são tratados como UDP.

 

Os pacotes TCP enviados por soquetes brutos são tratados da mesma forma que o tráfego UDP. Ou seja, somente o primeiro TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) e o primeiro TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) em soquetes brutos serão filtrados.

## <a name="flow_established"></a>FLOW \_ ESTABLISHED

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ FLOW ESTABLISHED \_ \_ \| V{4 6}**](management-filtering-layer-identifiers-.md) é corresponder após a conclusão bem-sucedida de um handshake TCP de três vias. Para o tráfego não TCP, o filtro é corresponder imediatamente depois que os filtros das camadas **AUTH \_ RECV \_ ACCEPT** ou **AUTH \_ CONNECT** são corresponderem.

Um filtro nessa camada não deve retornar Bloquear ou Permitir.

Essa camada é usada por drivers de texto explicação para controlar o estado da conexão, descrita em detalhes na [documentação Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="resource_release"></a>VERSÃO DO \_ RECURSO

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ RESOURCE RELEASE \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) **é \_** corresponder depois que os recursos alocados por meio da ATRIBUIÇÃO DE RECURSOS foram liberados.

## <a name="endpoint_closure"></a>FECHAMENTO DO \_ PONTO DE EXTREMIDADE

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ ENDPOINT \_ CLOSURE \_ \| V{4 6}**](management-filtering-layer-identifiers-.md) é corresponder quando um fluxo TCP conectado ou o ponto de extremidade de soquetes UDP é fechado.

## <a name="connect_redirect"></a>REDIRECIONAMENTO \_ DE CONEXÃO

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) permite a modificação de portas e endereços remotos. A conexão de saída será redirecionada durante essa conexão.

## <a name="bind_redirect"></a>REDIRECIONAMENTO \_ DE VINCULAÇÃO

Um filtro na camada [**FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) permite a modificação do endereço local e das portas do soquete subjacente. O soquete local será redirecionado durante o tempo de vida do soquete

## <a name="ale-discard-layers"></a>Camadas ALE DISCARD

Para cada uma das camadas ALE descritas acima, o mecanismo de filtragem contém uma camada de descarte correspondente. As camadas de descarte ALE são usadas por callouts para fins de registro em log. Pacotes e indicações que foram descartados em uma das camadas de filtragem ALE são indicados para a camada de descarte ALE correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Imposição de camada de aplicativo (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtragem com estado ALE](ale-stateful-filtering.md)
</dt> <dt>

[Tráfego multicast/difusão ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Reautorização de ALE](ale-re-authorization.md)
</dt> <dt>

[Personalização de Flow ALE](ale-flow-customization.md)
</dt> <dt>

[Fluxos de pacotes TCP](tcp-packet-flows.md)
</dt> <dt>

[Fluxos de pacotes UDP](udp-packet-flows.md)
</dt> <dt>

[Funções Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Filtrando sinalizadores de condição**](filtering-condition-flags-.md)
</dt> <dt>

[**Condições de filtragem disponíveis em cada camada de filtragem**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 