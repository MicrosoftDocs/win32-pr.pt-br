---
description: Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é o fornecimento de indicações ao cliente quando determinados eventos de rede ocorreram.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificação de eventos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827104"
---
# <a name="notification-of-network-events"></a>Notificação de eventos de rede

Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é o fornecimento de indicações ao cliente quando determinados eventos de rede ocorreram. A lista de eventos de rede definidos consiste no seguinte:

-   **FD \_ CONECTAR**– uma conexão a um host remoto ou a uma sessão de multicast foi concluída.
-   **FD \_ ACEITAR**— um host remoto está fazendo uma solicitação de conexão.
-   **FD \_ LEITURA**— dados de rede recebidos que estão disponíveis para serem lidos.
-   **FD \_ GRAVAÇÃO**— o espaço se tornou disponível nos buffers do provedor de serviços para que os dados adicionais possam ser enviados agora.
-   **FD \_ OOB**– os dados fora da banda estão disponíveis para leitura.
-   **FD \_ FECHAR**– o host remoto fechou a conexão.
-   **FD \_ QOS**— ocorreu uma alteração em níveis de QoS negociados.
-   **FD \_ \_QoS de grupo**– reservado.
-   **FD \_ \_ \_ Alteração de interface de roteamento**— uma interface local que deve ser usada para alcançar o destino especificado em sio de **\_ \_ \_ alteração de interface de roteamento de entrada** foi alterada.
-   **FD \_ \_ \_ Alteração da lista de endereços**— a lista de endereços locais aos quais o aplicativo pode ser associado foi alterada.

O conjunto de eventos de rede enumerado acima é, às vezes, chamado de eventos **FD \_ xxx** . A indicação da ocorrência de um ou mais desses eventos de rede pode ser fornecida de várias maneiras, dependendo de como o cliente solicita a notificação.

 

 



