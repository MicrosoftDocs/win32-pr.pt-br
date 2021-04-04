---
title: Filtragem de estado de ALE
description: Os filtros instalados nas camadas de aplicação da camada de aplicativo (EPA) da Windows Filtering Platform (WFP) executam a filtragem de rede com estado.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007545"
---
# <a name="ale-stateful-filtering"></a>Filtragem de estado de ALE

Os filtros instalados nas camadas de aplicação da camada de aplicativo (EPA) da Windows Filtering Platform (WFP) executam a filtragem de rede com estado. Um *fluxo Ale* é usado como a base para a filtragem de estado da Ale.

Um fluxo ALE é uma maneira de classificar o tráfego de rede agrupando-o com base em um endereço IP de origem, um endereço IP de destino, uma porta de origem, uma porta de destino e um protocolo. Um fluxo ALE poderia ser genérico, ou seja, um ou mais dos descritores poderiam corresponder a tudo (ou curinga \* ). Por exemplo, um fluxo de EPA de UDP genérico seria descrito como endereço IP de origem = \* , endereço IP \* de destino =, porta de origem = \* , porta de destino = \* e protocolo = UDP.

Depois que uma conexão é autorizada (as conexões de entrada são autorizadas na camada [**FWPM \_ camada de \_ autenticação Ale de \_ \_ recepção \_ aceitação \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) e conexões de saída na camada **FWPM da \_ autenticação Ale de camadas do \_ \_ \_ \_ AMV {4 \| 6}** ), um fluxo Ale é criado de modo que o bloqueio de uma alteração de política, todos os pacotes, entrada e saída, que pertencem ao mesmo fluxo Como uma alteração de política pode exigir o bloqueio de conexões anteriormente permitidas, os fluxos ALE precisam ser [reautorizados](ale-re-authorization.md) quando ocorre uma alteração de política.

A filtragem de estado da ALE reduz drasticamente o número de classificações necessárias classificando apenas o primeiro pacote que pertence a um fluxo ALE. Por comparação, a filtragem sem monitoração de Estado requer a classificação de cada pacote que atravessa a rede.

Um fluxo ALE tem uma direção associada, que é a direção do primeiro pacote do fluxo. Isso permite políticas mais flexíveis, permitindo que conexões iniciadas de entrada tenham políticas diferentes de conexões iniciadas de saída.

## <a name="tcp-ale-flow"></a>Fluxo de ALE TCP

Um fluxo ALE para tráfego TCP é identificado por cinco tuplas de TCP/IP (endereço IP de origem, endereço IP de destino, porta de origem, porta de destino e protocolo).

Um fluxo ALE TCP tem o mesmo tempo de vida que um soquete TCP conectado. Um soquete TCP conectado pode ser um soquete criado usando [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou um soquete criado como resultado de uma chamada [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

A EPA mantém uma relação um-para-um entre um fluxo de TCP ALE e um bloco de controle TCP (TCB).

## <a name="udp-ale-flow"></a>Fluxo de ALE UDP

> [!Note]  
> Protocolos que não são TCP ou ICMP são tratados como UDP.

 

Um fluxo ALE para o tráfego UDP é identificado por cinco tuplas de TCP/IP (endereço IP de origem, endereço IP de destino, porta de origem, porta de destino e protocolo).

Um fluxo de ALE UDP é criado com base em um soquete UDP e representa o ponto remoto com o qual o aplicativo está se comunicando. Um par remoto é identificado por uma tupla (endereço IP de destino e porta de destino).

Há uma relação um-para-muitos entre um soquete UDP e os pares remotos aos quais ele se comunica.

Quando o soquete UDP local for fechado, todos os fluxos ALE associados a ele serão excluídos.

Na ausência de fechamentos de soquete, os fluxos ALE de unicast UDP têm um tempo limite de ociosidade [configurável](ale-flow-customization.md) que usa por padrão 60 segundos. Se nenhum pacote for enviado ou recebido nessa janela, o fluxo ALE será excluído. Esse tempo limite padrão é progressivamente reduzido quando o número de fluxos ALE em todo o sistema atinge um determinado limite.

## <a name="icmp-ale-flow"></a>Fluxo de ALE ICMP

Um fluxo ALE para tráfego ICMP é identificado por seis tuplas (endereço IP de origem, endereço IP de destino, tipo de ICMP, código ICMP, protocolo e ID de ICMP). A ID de ICMP faz parte do fluxo de ALE somente para o tráfego de eco/resposta ICMP.

Na ausência de fechamentos de soquete, os fluxos ALE de unicast ICMP têm um tempo limite de ociosidade [configurável](ale-flow-customization.md) cujo padrão é de 60 segundos. Se nenhum pacote for enviado ou recebido nessa janela, o fluxo ALE será excluído. Esse tempo limite padrão é progressivamente reduzido quando o número de fluxos ALE em todo o sistema atinge um determinado limite.

Somente as mensagens ICMP que não são de erro são indicadas para camadas ALE. Mensagens de erro ICMP podem ser inspecionadas em \_ camadas de erro ICMP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação da camada de aplicativo (EPA)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Camadas ALE](ale-layers.md)
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
</dt> </dl>

 

 