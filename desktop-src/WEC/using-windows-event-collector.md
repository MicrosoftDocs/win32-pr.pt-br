---
title: Usando o coletor de eventos do Windows
description: Esta seção lista os tópicos que explicam as tarefas que podem ser realizadas usando o SDK do coletor de eventos do Windows. Exemplos de código e explicações para todas as tarefas são incluídos em cada um dos tópicos a seguir.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788824"
---
# <a name="using-windows-event-collector"></a>Usando o coletor de eventos do Windows

Esta seção lista os tópicos que explicam as tarefas que podem ser realizadas usando o SDK do coletor de eventos do Windows. Exemplos de código e explicações para todas as tarefas são incluídos em cada um dos tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção

-   [Criando uma assinatura iniciada pelo coletor](creating-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para criar uma assinatura iniciada pelo coletor. Uma assinatura iniciada pelo coletor permite que você receba eventos em um computador local (o coletor de eventos) que são encaminhados de um computador remoto (uma origem do evento).

-   [Configurando uma assinatura iniciada pela origem](setting-up-a-source-initiated-subscription.md)

    Fornece informações e um exemplo de código C++ para criar uma assinatura iniciada pela fonte. Uma assinatura iniciada pela origem permite que você receba eventos em um computador local (o coletor de eventos) que são encaminhados de um computador remoto (uma origem do evento) sem especificar as origens do evento na assinatura.

-   [Adicionando uma origem do evento a uma assinatura iniciada pelo coletor](adding-an-event-source-to-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para adicionar uma origem de evento (computador local ou computador remoto) a uma assinatura iniciada pelo coletor. Uma assinatura iniciada pelo coletor não pode iniciar a coleta de eventos até que uma origem do evento seja adicionada à assinatura.

-   [Criando assinaturas de evento de hardware](creating-hardware-event-subscriptions.md)

    Fornece informações sobre como criar uma assinatura de evento para receber eventos de hardware de um computador que tenha um controlador BMC (Baseboard Management Controller) instalado.

-   [Excluindo uma assinatura do coletor de eventos](deleting-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para excluir uma assinatura do coletor de eventos de um computador local.

-   [Exibindo as propriedades de uma assinatura do coletor de eventos](displaying-the-properties-of-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para exibir os valores de propriedade de uma assinatura do coletor de eventos. Os valores de propriedade podem fornecer informações úteis, como os endereços de origens do evento, o status da assinatura e as origens do evento e informações sobre como os eventos são entregues.

-   [Exibindo o status de uma assinatura do coletor de eventos](displaying-the-status-of-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para exibir o status de tempo de execução de fontes de eventos que estão associadas a uma assinatura do coletor de eventos. Isso permite que você exiba mensagens de erro que podem ajudar a resolver problemas, o que impede que uma fonte de eventos encaminhe eventos.

-   [Listando assinaturas do coletor de eventos](listing-event-collector-subscriptions.md)

    Fornece informações e um exemplo de código C++ para listar as assinaturas que existem em um computador local. Você pode usar os nomes de assinatura que são obtidos com este exemplo para excluir uma assinatura, adicionar uma origem de evento a uma assinatura, recuperar as propriedades de uma assinatura ou exibir o status de uma assinatura.

-   [Removendo uma origem do evento de uma assinatura iniciada pelo coletor](removing-an-event-source-from-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para remover uma origem de evento de uma assinatura iniciada pelo coletor. Você pode remover uma fonte de eventos de uma assinatura iniciada pelo coletor sem desabilitar a assinatura.

-   [Repetindo uma assinatura do coletor de eventos](retrying-an-event-collector-subscription.md)

    Fornece informações e um exemplo de código C++ para repetir uma assinatura do coletor de eventos quando uma ou mais origens de evento falharam. Você pode repetir uma única origem de evento ou pode repetir a assinatura inteira.

 

 




