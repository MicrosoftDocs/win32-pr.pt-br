---
description: Processo de notificações no Windows Search
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Processo de notificações no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b37747d1ec13c3a4a865e16721c64d4a0186dbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089814"
---
# <a name="notifications-process-in-windows-search"></a>Processo de notificações no Windows Search

Este tópico é organizado da seguinte maneira:

-   [Visão geral do processo de notificações](#overview-of-the-notifications-process)
-   [Rastreamentos](#crawls)
-   [Notificações gerenciadas pelo indexador](#indexer-managed-notifications)
-   [Notificações gerenciadas pelo provedor](#provider-managed-notifications)
-   [Notificações em conjuntos de linhas](#notifications-on-rowsets)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-the-notifications-process"></a>Visão geral do processo de notificações

Há três abordagens pelas quais os dados do seu armazenamento de dados podem ser indexados:

-   Rastreamentos
-   Notificações gerenciadas pelo indexador
-   Notificações gerenciadas pelo provedor

Os méritos de cada abordagem são descritos nas seções a seguir.

## <a name="crawls"></a>Rastreamentos

As fontes habilitadas para notificação fazem um rastreamento incremental na inicialização e, em seguida, dependem das notificações ou de um comando explícito para rastrear novamente. Isso ocorre automaticamente no Windows Vista e versões posteriores. Em sistemas operacionais anteriores ao Windows Vista, você deve configurar um evento agendado no [Agendador de tarefas](../taskschd/task-scheduler-start-page.md) que chama seu código para iniciar um rastreamento em suas páginas de início. Você não precisa implementar nenhuma forma de notificações. Como um processo em segundo plano, o indexador atravessa seu escopo de rastreamento, procurando alterações e atualizando o catálogo. Essa opção é recomendada para quase todas as situações.

## <a name="indexer-managed-notifications"></a>Notificações de Indexer-Managed

Com as notificações gerenciadas pelo indexador, você implementa uma estratégia de notificação que notifica o indexador quando os dados no armazenamento de dados são alterados e o indexador gerencia as notificações e a indexação dos dados. Nessa situação, o componente (que chamamos de um provedor de notificações) monitora o armazenamento de dados, coleta informações sobre alterações na loja e notifica periodicamente o indexador com uma lista de itens que precisam de indexação. O indexador é responsável por recuperar e resolver notificações em caso de falha. Essa opção, que você pode considerar como a estratégia "enviar e esquecer", reduz a frequência dos rastreamentos do indexador.

## <a name="provider-managed-notifications"></a>Notificações de Provider-Managed

Com notificações gerenciadas por provedor, você implementa uma estratégia de notificação que é semelhante à segunda abordagem, exceto que seu provedor de notificações deve controlar as notificações e é responsável por recuperar e resolver notificações em caso de falha. Nessa situação, o provedor de notificações monitora o armazenamento de dados, coleta e mantém informações sobre alterações na loja, notifica periodicamente o indexador com uma lista de itens que precisam de indexação, recebe atualizações de status do indexador e envia notificações novamente em caso de falha.

> [!Note]  
> Essa opção **não é recomendada a menos** que você espere que os rastreamentos incrementais de seu armazenamento de dados atrapalhem significativamente o desempenho, e você precisa de controle granular ou insight do status de indexação.

 

## <a name="notifications-on-rowsets"></a>Notificações em conjuntos de linhas

No Windows 7 e posterior, a indexação de eventos permite que os provedores recebam notificações sobre seus conjuntos de linhas. Provedores que usam eventos de indexação podem manter seus conjuntos de linhas de maneira semelhante ao comportamento de locais reais do sistema de arquivos. Bibliotecas e pesquisas são os principais exemplos de locais de não-sistema de arquivos no Windows 7. O evento do indexador é para as exibições de biblioteca, pois as notificações são para exibições de pasta de arquivos. A interface [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) deve ser implementada para receber notificações de eventos. A camada de dados é o cliente primário do indexador de eventos e decide o que fazer com os eventos na interface do usuário do modo de exibição de itens. Para obter mais informações, consulte [indexação de índices e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md).

Por outro lado, no Windows Vista, as exibições baseadas em consulta não têm eventos associados, exceto para o cache do Shell para edições de propriedade de arquivo. Quando você executa uma pesquisa, os resultados retornados são estáticos. Portanto, se outro documento for adicionado ao seu sistema que corresponda ao seu termo de pesquisa, sua exibição não será atualizada para incluir a nova adição. Esse comportamento é padrão para resultados estáticos baseados na Web. No entanto, os resultados estáticos são menos aceitáveis quando você está tentando fornecer uma exibição baseada em consulta em um local de armazenamento. Os usuários esperam que o conteúdo do indexador seja atual. Para obter mais informações, consulte [notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md). Para obter a documentação de referência, consulte [interfaces de notificações](-search-notifications-interfaces-entry-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[O que está incluído no índice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de indexação no Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de consulta no Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Requisitos de formatação de URL](url-formatting-requirements.md)
</dt> </dl>

 

 
