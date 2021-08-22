---
description: Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é fornecer indicações ao cliente quando determinados eventos de rede ocorreram.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notificação de eventos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794756"
---
# <a name="notification-of-network-events"></a>Notificação de eventos de rede

Uma das responsabilidades mais importantes de um provedor de serviços de transporte de dados é fornecer indicações ao cliente quando determinados eventos de rede ocorreram. A lista de eventos de rede definidos consiste no seguinte:

-   **FD \_ CONNECT**— uma conexão com um host remoto ou com uma sessão multicast foi concluída.
-   **FD \_ ACCEPT**— um host remoto está fazendo uma solicitação de conexão.
-   **FD \_ READ**— Os dados de rede chegaram, que estão disponíveis para serem lidos.
-   **FD \_ WRITE**— O espaço ficou disponível nos buffers do provedor de serviços para que dados adicionais agora possam ser enviados.
-   **FD \_ OOB**— Dados fora de banda estão disponíveis para serem lidos.
-   **FD \_ CLOSE**— o host remoto fechou a conexão.
-   **FD \_ QOS**— Ocorreu uma alteração em níveis negociados de QoS.
-   **FD \_ GROUP \_ QOS**— Reservado.
-   **FD \_ ALTERAÇÃO \_ DA INTERFACE \_ DE** ROTEAMENTO — uma interface local que deve ser usada para alcançar o destino especificado em **\_ \_ \_ IOCTL** de ALTERAÇÃO da INTERFACE DE ROTEAMENTO SIO foi alterada.
-   **FD \_ ALTERAÇÃO \_ DE \_ LISTA DE** ENDEREÇOS – a lista de endereços locais aos quais o aplicativo pode ser associado foi alterada.

Às vezes, o conjunto de eventos de rede enumerados acima é chamado de **eventos FD \_ XXX.** A indicação da ocorrência de um ou mais desses eventos de rede pode ser dada de várias maneiras, dependendo de como o cliente solicita a notificação.

 

 



