---
description: O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados são determinados.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828810"
---
# <a name="tcpip-characteristics"></a>Características de TCP/IP

O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados são determinados. Essas características podem ser combinadas com opções de desenvolvimento que resultam em baixo desempenho. O impacto que essas características de TCP/IP têm em um aplicativo depende se o aplicativo é transacional ou de streaming.

Os aplicativos transacionais são afetados pela sobrecarga necessária para o estabelecimento e o encerramento da conexão. Por exemplo, cada vez que uma conexão é estabelecida em uma rede Ethernet, três pacotes de aproximadamente 60 bytes devem ser enviados e aproximadamente um RTT é necessário para a troca. Quando ocorre a rescisão de uma conexão, quatro pacotes são trocados. Isso é para cada conexão; um aplicativo que abre e fecha as conexões geralmente incorre nessa sobrecarga em cada ocorrência.

Outro aspecto do TCP/IP é o *início lento*, que ocorre sempre que uma conexão é estabelecida. O início lento é um limite artificial no número de segmentos de dados que podem ser enviados antes de a confirmação desses segmentos ser recebida. O início lento é projetado para limitar o congestionamento da rede. Quando uma conexão pela Ethernet é estabelecida, independentemente do tamanho da janela do destinatário, uma transmissão de 4 KB pode levar até 3-4 RTT devido ao início lento.

Uma otimização de TCP/IP chamada de algoritmo Nagle também pode limitar a velocidade de transferência de dados em uma conexão. O algoritmo Nagle foi projetado para reduzir a sobrecarga de protocolo para aplicativos que enviam pequenas quantidades de dados, como Telnet, que envia um único caractere por vez. Em vez de enviar imediatamente um pacote com muitos cabeçalhos e pequenos dados, a pilha aguarda mais dados do aplicativo ou uma confirmação antes de continuar.

As confirmações atrasadas, conhecidas como *ACK atrasada*, também são projetadas no TCP/IP para permitir o acúmulo mais eficiente de confirmações quando os dados de retorno estão em breve do aplicativo do lado de recebimento. Infelizmente, se esses dados não estiverem em breve e o lado de envio estiver aguardando uma confirmação, poderão ocorrer atrasos de aproximadamente 200 milissegundos por envio.

Quando uma conexão TCP é fechada, os recursos de conexão no nó que iniciou o fechamento são colocados em um estado de espera, chamado espera de tempo, para proteger contra corrupção de dados se os pacotes duplicados permanecerem na rede. Isso garante que ambas as extremidades sejam concluídas com a conexão. Isso pode causar esgotamento de recursos necessários por conexão, como RAM e portas, quando os aplicativos abrem e fecham conexões com frequência.

Além de ser afetado pela confirmação atrasada e por outros esquemas de prevenção de congestionamento, os aplicativos de streaming também podem ser afetados por um tamanho de janela de recepção padrão muito pequeno na extremidade de recebimento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comportamento do aplicativo](application-behavior-2.md)
</dt> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



