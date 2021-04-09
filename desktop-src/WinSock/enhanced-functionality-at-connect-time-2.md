---
description: O Windows Sockets 2 oferece um conjunto expandido de operações que podem ocorrer coincidentes para estabelecer uma conexão de soquete. Os requisitos do provedor de serviços para implementar esses recursos são descritos abaixo.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Funcionalidade aprimorada no momento da conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090396"
---
# <a name="enhanced-functionality-at-connect-time"></a>Funcionalidade aprimorada no momento da conexão

O Windows Sockets 2 oferece um conjunto expandido de operações que podem ocorrer coincidentes para estabelecer uma conexão de soquete. Os requisitos do provedor de serviços para implementar esses recursos são descritos abaixo.

## <a name="conditional-acceptance"></a>Aceitação condicional

Conforme descrito anteriormente, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) invoca uma função de condição fornecida pelo cliente que usa parâmetros de entrada para fornecer informações sobre a solicitação de conexão pendente. Essas informações podem ser usadas pelo cliente para aceitar ou rejeitar uma solicitação de conexão com base em informações do chamador, como identificador de chamada, QoS, etc. Se a função Condition retornar o CF \_ Accept, um novo soquete será criado com as mesmas propriedades que o soquete de escuta e um identificador para o novo soquete será retornado. Se a função Condition retornar o \_ rejeição de CF, a solicitação de conexão deverá ser rejeitada. Se a função Condition retornar o \_ adiamento de CF, a decisão de aceitar/rejeitar não poderá ser feita imediatamente e o provedor de serviços deverá deixar a solicitação de conexão na fila de pendências. O cliente deve chamar **WSPAccept** novamente, quando estiver pronto para tomar uma decisão e organizar a função Condition para retornar a recusa de CF \_ Accept ou CF \_ . Embora uma solicitação de conexão adiada esteja na parte superior da fila da lista de pendências, o provedor de serviços não emite nenhuma outra indicações para solicitações de conexão pendentes.

## <a name="exchanging-user-data-at-connect-time"></a>Trocando dados do usuário no momento da conexão

Alguns protocolos permitem que uma pequena quantidade de dados do usuário seja trocada no momento do Connect. Se esses dados tiverem sido recebidos do host de conexão, eles serão colocados em um buffer do provedor de serviços e um ponteiro para esse buffer junto com um valor de comprimento será fornecido ao cliente SPI do Winsock por meio de parâmetros de entrada para a função de condição [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) . Se o cliente SPI do Winsock tiver dados de resposta para retornar ao host de conexão, ele poderá copiá-lo em um buffer fornecido pelo provedor de serviços. Um ponteiro para esse buffer e um inteiro que indica o tamanho do buffer também são fornecidos como parâmetros de entrada de função de condição (se houver suporte para o protocolo).

## <a name="establishing-socket-groups"></a>Estabelecendo grupos de soquetes

Todo o uso de grupos de soquetes é reservado.

 

 



