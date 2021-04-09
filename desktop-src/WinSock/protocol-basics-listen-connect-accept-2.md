---
description: Noções básicas de protocolo de WSPListen, WSPAccept e WSPConnect para estabelecer uma conexão de soquete com o Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Noções básicas de protocolo: escutar, conectar, aceitar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62ef290d71e571154b4d022c24c7e21f8fffa1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090363"
---
# <a name="protocol-basics-listen-connect-accept"></a>Noções básicas de protocolo: escutar, conectar, aceitar

As operações básicas envolvidas com o estabelecimento de uma conexão de soquete podem ser mais convenientemente explicadas em termos do paradigma do cliente-servidor.

O lado do servidor primeiro criará um soquete, o associará a um endereço local conhecido (para que o cliente possa encontrá-lo) e colocará o soquete no modo de escuta, por meio de [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), para se preparar para todas as solicitações de conexão de entrada e para especificar o comprimento da fila de pendências de conexão. Os provedores de serviço mantêm solicitações de conexão pendentes em uma fila de lista de pendências até que sejam acionados pelo servidor ou retirados (devido a um tempo limite) pelo cliente. Um provedor de serviços pode ignorar silenciosamente as solicitações para estender o tamanho da fila de pendências além de um limite superior definido pelo provedor.

Neste ponto, se um soquete de bloqueio estiver sendo usado, o lado do servidor poderá chamar imediatamente o [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) , que será bloqueado até que uma solicitação de conexão esteja pendente. Por outro lado, o servidor também pode usar um dos mecanismos de indicação de evento de rede discutidos anteriormente para organizar a notificação de solicitações de conexão de entrada. Dependendo do mecanismo de notificação selecionado, o provedor emitirá uma mensagem do Windows ou sinalizará um objeto de evento quando as solicitações de conexão chegarem. Consulte a [notificação de eventos de rede](notification-of-network-events-2.md) para saber como registrar-se para o \_ evento de aceitação de rede FD.

O lado do cliente criará um soquete apropriado e iniciará a conexão chamando [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)), especificando o endereço do servidor conhecido. Geralmente, os clientes não executam uma operação de [**ligação**](/windows/desktop/api/winsock/nf-winsock-bind) explícita antes de iniciar uma conexão, permitindo que o provedor de serviços execute uma ligação implícita em seu nome. Se o soquete estiver no modo de bloqueio, o **WSPConnect** será bloqueado até que o servidor tenha recebido e aprovado na solicitação de conexão (ou até ocorrer um tempo limite). Caso contrário, o cliente deve usar um dos mecanismos de indicação de evento de rede discutidos anteriormente para organizar a notificação de uma nova conexão estabelecida. Dependendo do mecanismo de notificação selecionado, o provedor indicará isso por meio de uma mensagem do Windows ou sinalizando um objeto de evento.

Quando o lado do servidor invoca [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept), o provedor de serviços chama a função de condição fornecida pelo aplicativo, usando parâmetros de função para passar as informações do servidor da entrada superior na fila de pendências de solicitação de conexão. Essas informações incluem itens como endereço de host de conexão, qualquer dado de usuário disponível e qualquer informação de QoS disponível. Usando essas informações, a função Condition do servidor determina se deve aceitar a solicitação, rejeitar a solicitação ou adiar a tomada de decisão até mais tarde. Essa decisão é indicada por meio do valor de retorno da função Condition. Consulte a [notificação de eventos de rede](notification-of-network-events-2.md) para saber como registrar- \_ se no evento de rede do FD Connect.

Se o servidor decidir aceitar a solicitação, o provedor deverá criar um novo soquete com todos os mesmos atributos e registros de eventos que o soquete de escuta. O soquete original permanece no estado de escuta para que as solicitações de conexão subsequentes possam ser recebidas. Por meio de parâmetros de saída da função Condition, o servidor também pode fornecer quaisquer dados do usuário de resposta e atribuir parâmetros de QoS (supondo que essas operações sejam compatíveis com o provedor de serviços).

 

 
