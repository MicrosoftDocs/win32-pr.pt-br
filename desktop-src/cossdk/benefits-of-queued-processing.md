---
description: Benefícios do processamento em fila
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Benefícios do processamento em fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104565663"
---
# <a name="benefits-of-queued-processing"></a>Benefícios do processamento em fila

Ao projetar novos aplicativos, os desenvolvedores devem considerar as implicações dos componentes de codificação para processamento em tempo real (síncrono) versus processamento em fila (assíncrono). A escolha depende dos requisitos do aplicativo específico, conforme determinado pela lógica de negócios subjacente. Como uma diretriz, o processamento em fila oferece as seguintes vantagens em relação ao processamento em tempo real:

-   Dependência reduzida da disponibilidade do componente
-   Tempos de vida de componente mais curtos
-   Produtividade ininterrupta ao usar aplicativos desconectados
-   Confiabilidade da mensagem
-   Agendamento de servidor eficiente

## <a name="component-availability"></a>Disponibilidade do componente

Em um aplicativo de processamento em tempo real, se apenas um componente da transação não estiver disponível — talvez devido a problemas de sobrecarga ou de rede do servidor — todo o processo é bloqueado e não pode ser concluído. Por outro lado, um aplicativo que usa o serviço de componentes na fila COM+ separa a transação em atividades que devem ser concluídas agora e aquelas que podem ser concluídas posteriormente. Por exemplo, as mensagens podem ser enfileiradas para processamento posterior, para que o componente solicitante seja gratuito para outras tarefas.

## <a name="component-lifetimes"></a>Tempos de vida do componente

Um aplicativo que usa o serviço de componentes na fila permite que o componente do servidor opere independentemente do cliente. Como resultado, os componentes do servidor podem ser concluídos mais rapidamente. Em um sistema em tempo real, o componente de servidor existe desde o momento em que é criado até que o objeto seja finalmente liberado. O servidor aguarda que o cliente faça chamadas de método e que os resultados sejam retornados, o que nega o ciclo rápido de objetos de servidor e limita a escalabilidade do servidor.

## <a name="disconnected-applications"></a>Aplicativos desconectados

O uso crescente de laptops, notebooks e computadores Palm criou uma necessidade de aplicativos que se desconectam ocasionalmente clientes ou usuários móveis. Em um sistema enfileirado, esses usuários podem continuar a trabalhar em um cenário desconectado ou quando não estiverem conectados ao servidor, e poderão se conectar posteriormente aos bancos de dados ou servidores para processar suas solicitações. Por exemplo, um vendedor pode receber pedidos de clientes e, posteriormente, conectar-se ao departamento de remessa para processar esses pedidos.

Se você tiver um componente que pode ser executado conectado ou desconectado, as mensagens estão viajando em uma direção e raramente há necessidade de alternar para frente e para trás. Por exemplo, no cenário de ordem demorada, o componente de envio recebe a mensagem e a processa. Ele pode gerar outro componente para cobrança ou auditoria. O cliente é confirmado antes de o servidor ser iniciado. A mensagem não é enviada até que o aplicativo seja confirmado.

A ilustração a seguir mostra o fluxo de informações em um cenário desconectado.

![Diagrama que mostra o fluxo de informações entre o cliente e o servidor.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Confiabilidade da mensagem

O serviço de enfileiramento de mensagens é uma ferramenta poderosa que usa técnicas de banco de dados para ajudar a proteger o dado de maneira robusta. No caso de uma falha de servidor, o enfileiramento de mensagens garante que as transações sejam revertidas para que as mensagens não sejam perdidas e os dados não estejam corrompidos.

## <a name="server-scheduling"></a>Agendamento de servidor

Um aplicativo que usa componentes enfileirados é adequado para a execução de componentes com mudança de tempo, o que adia o trabalho não crítico para um período de fora de pico. Esse é o mesmo conceito útil que foi aplicado ao processamento de modo de lote tradicional. Solicitações semelhantes podem ser adiadas para execução contígua pelo servidor em vez de exigir que o servidor reaja imediatamente a uma ampla variedade de solicitações.

 

 



