---
description: O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados determinam.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f720dac1157149fe34da1b6bcbc08928654f268c7ac3e32b2e22599ae43cb701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733416"
---
# <a name="tcpip-characteristics"></a>Características de TCP/IP

O TCP/IP tem características que permitem que o protocolo opere conforme seus requisitos de implementação padronizados determinam. Essas características podem combinar com opções de desenvolvimento que resultam em baixo desempenho. O impacto que essas características de TCP/IP têm em um aplicativo depende se o aplicativo é transacional ou de streaming.

Os aplicativos transacionais são afetados pela sobrecarga necessária para o estabelecimento e o encerramento da conexão. Por exemplo, sempre que uma conexão é estabelecida em uma rede Ethernet, três pacotes de aproximadamente 60 bytes cada devem ser enviados e aproximadamente um RTT é necessário para a troca. Quando ocorre o encerramento de uma conexão, quatro pacotes são trocados. Isso é para cada conexão; um aplicativo que abre e fecha conexões geralmente incorre nessa sobrecarga em cada ocorrência.

Outro aspecto do TCP/IP é *o início lento,* que ocorre sempre que uma conexão é estabelecida. O início lento é um limite artificial no número de segmentos de dados que podem ser enviados antes que a confirmação desses segmentos seja recebida. O início lento foi projetado para limitar o congestionamento de rede. Quando uma conexão via Ethernet é estabelecida, independentemente do tamanho da janela do receptor, uma transmissão de 4 KB pode levar de 3 a 4 RTT devido ao início lento.

Uma otimização de TCP/IP chamada Algoritmo Nagle também pode limitar a velocidade de transferência de dados em uma conexão. O Algoritmo Nagle foi projetado para reduzir a sobrecarga de protocolo para aplicativos que enviam pequenas quantidades de dados, como o Telnet, que envia um único caractere por vez. Em vez de enviar imediatamente um pacote com muitos header e poucos dados, a pilha aguarda mais dados do aplicativo, ou uma confirmação, antes de continuar.

As confirmações atrasadas, normalmente conhecidas como *ACK* atrasadas, também são projetadas em TCP/IP para habilitar o coframento mais eficiente de confirmações quando os dados de retorno são recebidos do aplicativo do lado receptor. Infelizmente, se esses dados não são futuros e o lado de envio está aguardando uma confirmação, podem ocorrer atrasos de aproximadamente 200 milissegundos por envio.

Quando uma conexão TCP é fechada, os recursos de conexão no nó que iniciou o fechamento são colocados em um estado de espera, chamado TIME-WAIT, para se proteger contra dados de corrupção se os pacotes duplicados permanecerem na rede. Isso garante que ambas as extremidades sejam concluídas com a conexão. Isso pode causar o esgotamento dos recursos necessários por conexão, como RAM e portas, quando os aplicativos abrem e fecham conexões com frequência.

Além de serem afetados por ACK atrasado e outros esquemas de evitar congestionamento, os aplicativos de streaming também podem ser afetados por um tamanho de janela de recebimento padrão muito pequeno na extremidade de recebimento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comportamento do aplicativo](application-behavior-2.md)
</dt> <dt>

[Aplicativos de soquetes Windows de alto desempenho](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



