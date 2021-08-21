---
description: Benefícios do processamento em fila
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Benefícios do processamento em fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c41d902d9e72af40b70ccc95efe33e2857c8ef07953c70ef1fc0879ba676ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308776"
---
# <a name="benefits-of-queued-processing"></a>Benefícios do processamento em fila

Ao projetar novos aplicativos, os desenvolvedores devem considerar as implicações dos componentes de codificação para processamento em tempo real (síncrono) versus processamento enxuado (assíncrono). A escolha depende dos requisitos do aplicativo específico, conforme determinado pela lógica de negócios subjacente. Como diretriz, o processamento na fila oferece as seguintes vantagens em relação ao processamento em tempo real:

-   Dependência reduzida da disponibilidade do componente
-   Tempo de vida do componente mais curto
-   Produtividade ininterrupta ao usar aplicativos desconectados
-   Confiabilidade da mensagem
-   Agendamento de servidor eficiente

## <a name="component-availability"></a>Disponibilidade do componente

Em um aplicativo de processamento em tempo real, se apenas um componente da transação não estiver disponível , talvez devido à sobrecarga do servidor ou problemas de rede, todo o processo será bloqueado e não poderá ser concluído. Por outro lado, um aplicativo que usa o serviço de componentes em fila COM+ separa a transação em atividades que devem ser concluídas agora e aquelas que podem ser concluídas posteriormente. Por exemplo, as mensagens podem ser en fila para processamento posterior para que o componente solicitante seja livre para outras tarefas.

## <a name="component-lifetimes"></a>Tempo de vida do componente

Um aplicativo que usa o serviço de componentes na fila permite que o componente de servidor opere independentemente do cliente. Como resultado, os componentes do servidor podem ser concluídos mais rapidamente. Em um sistema em tempo real, o componente de servidor existe desde o momento em que ele é criado até que o objeto seja finalmente liberado. O servidor aguarda que o cliente faça chamadas de método e que os resultados sejam retornados, o que nega o ciclo rápido de objetos de servidor e limita a escalabilidade do servidor.

## <a name="disconnected-applications"></a>Aplicativos desconectados

O uso cada vez maior de laptops, notebooks e computadores de mão de trabalho criou uma necessidade de aplicativos que a serviço ocasionalmente desconectaram clientes ou usuários móveis. Em um sistema na fila, esses usuários podem continuar a trabalhar em um cenário desconectado ou quando não estão conectados ao servidor e podem se conectar posteriormente aos bancos de dados ou servidores para processar suas solicitações. Por exemplo, um vendedor pode receber pedidos de clientes e, posteriormente, conectar-se ao departamento de remessa para processar esses pedidos.

Se você tiver um componente que pode ser executado conectado ou desconectado, as mensagens estão viajando em uma direção e raramente há a necessidade de alternar para frente e para trás. Por exemplo, no cenário de tomada de pedido, o componente de remessa recebe a mensagem e a processa. Ele pode gerar outro componente para cobrança ou auditoria. O cliente faz commits antes de o servidor ser iniciado. A mensagem não é enviada até que o aplicativo seja commit.

A ilustração a seguir mostra o fluxo de informações em um cenário desconectado.

![Diagrama que mostra o fluxo de informações entre o cliente e o servidor.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Confiabilidade da mensagem

O En fila de mensagens é uma ferramenta poderosa que usa técnicas de banco de dados para ajudar a proteger os dados de maneira robusta. No caso de uma falha do servidor, o En enrosamento de mensagens garante que as transações sejam regredidas para que as mensagens não sejam perdidas e os dados não sejam corrompidos.

## <a name="server-scheduling"></a>Agendamento de servidor

Um aplicativo que usa componentes na fila é adequado para a execução de componentes com deslocamento de tempo, o que adia o trabalho não crítico para um período fora do pico. Esse é o mesmo conceito útil que foi aplicado ao processamento de modo de lote tradicional. Solicitações semelhantes podem ser adiadas para execução contígua pelo servidor em vez de exigir que o servidor reaja imediatamente a uma ampla variedade de solicitações.

 

 



