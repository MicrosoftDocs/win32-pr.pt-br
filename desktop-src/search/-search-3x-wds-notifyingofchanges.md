---
description: o uso dos componentes de APIs de notificação pode notificar o indexador de que um item foi alterado, movido ou excluído e pode adicionar escopos de pesquisa à fila de URLs do indexador de pesquisa da Windows que exigem indexação.
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: notificando o índice de alterações (Windows pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb386763be5192851368b1f46b69f94576fbe261a57d215d649d38ac5a19ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052223"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>notificando o índice de alterações (Windows pesquisa)

o uso dos componentes de APIs de notificação pode notificar o indexador de que um item foi alterado, movido ou excluído e pode adicionar escopos de pesquisa à fila de URLs do indexador de pesquisa da Windows que exigem indexação.

os componentes do podem notificar os Windows indexador de pesquisa de que os dados em seu armazenamento foram alterados. Normalmente, você pode contar com os rastreamentos agendados do indexador. No entanto, o fornecimento de notificações ao indexador pode melhorar o desempenho, garantindo que o indexador não rastreie toda a loja em índices incrementais. Por exemplo, isso pode ser recomendado se você espera que o armazenamento de dados seja excepcionalmente grande e/ou intensamente ocupado, como um armazenamento de dados de email, por exemplo.

-   [Implementando notificações gerenciadas pelo indexador](#implementing-indexer-managed-notifications)
    -   [Fila de notificações](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [Implementando notificações gerenciadas pelo provedor](#implementing-provider-managed-notifications)
    -   [Fila de notificações](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>Implementando notificações gerenciadas pelo indexador

As notificações gerenciadas pelo indexador permitem que você controle o acesso ao seu armazenamento de dados enquanto libera você de manter a fila de notificações em todo o processo de indexação. Seu provedor de notificações deve monitorar as alterações no armazenamento de dados e criar uma fila de notificações. Periodicamente, seu provedor envia um lote de notificações de alteração para o indexador. Quando o indexador recebe suas notificações, ele retorna uma confirmação e você pode remover o (s) item (ns) da sua fila. Se, após um período de tempo, você não receber uma confirmação, poderá enviar novamente as notificações. Em caso de falha, o indexador recria sua fila interna de itens para rastrear ou executa um rastreamento incremental da loja.

Para implementar notificações gerenciadas pelo indexador, você precisa implementar o seguinte:

-   Um mecanismo para monitorar alterações no armazenamento de dados.
-   Uma estrutura de dados para enfileirar informações (várias estruturas de [**\_ \_ \_ alteração persistentes de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) ) sobre essas alterações.
-   Interface [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) para enviar suas notificações para o indexador e obter confirmações de notificação do indexador.

### <a name="notifications-queue"></a>Fila de notificações

Você precisa monitorar e enfileirar todas as alterações em seu armazenamento de dados para enviar ao indexador como uma notificação. Quantas notificações você coloca na fila e com que frequência elas são enviadas ao indexador depende de sua circunstância. Talvez você envie um lote de notificações para cada *n* números de alterações ou após um intervalo de tempo *t* ou uma combinação dos dois.

O indexador espera que as notificações sejam fornecidas em uma matriz de estruturas de [**\_ \_ \_ alteração persistentes de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) , portanto, você pode optar por implementar sua fila da mesma forma.

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

Para acessar essa interface, primeiro você cria uma instância de um objeto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obter acesso a um objeto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . A partir desse objeto **ISearchCatalogManager** , você cria uma instância de um objeto [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) e notifica o indexador das alterações de dados com uma chamada para o método **onitems** .

Na chamada para esse método, você inclui o número de alterações que estão sendo relatadas e uma matriz de estruturas de [**\_ \_ \_ alteração persistente de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) . Você obtém novamente uma matriz de códigos de conclusão de RH que indicam se cada URL foi aceita para indexação. Essa é a sua confirmação do indexador.

## <a name="implementing-provider-managed-notifications"></a>Implementando notificações gerenciadas pelo provedor

as notificações gerenciadas pelo provedor permitem que você controle o acesso ao seu armazenamento de dados e monitore o progresso do indexador à medida que ele atualiza o catálogo de pesquisa Windows. Seu provedor deve monitorar as alterações no armazenamento de dados e criar uma fila de notificações. Periodicamente, seu provedor envia um lote de notificações de alteração para o indexador. Quando o indexador recebe suas notificações, ele retorna uma confirmação. Se, após um período de tempo, você não receber uma confirmação, poderá enviar novamente as notificações. como o indexador rastreia o armazenamento de dados e atualiza o catálogo de pesquisa Windows, ele notifica seu provedor sobre cada atualização de catálogo e você pode remover os itens da sua fila. Seu provedor mantém sua fila de notificação em todo esse processo para que, em caso de falha, você possa reenviar notificações para o indexador.

Para implementar notificações gerenciadas pelo provedor, você precisa implementar o seguinte:

-   Um mecanismo para monitorar alterações no armazenamento de dados.
-   Uma estrutura de dados para colocar informações em fila (várias estruturas de [**\_ \_ alteração de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) ) sobre essas alterações.
-   Interface [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) para enviar suas notificações para o indexador e obter confirmações de notificação do indexador.
-   Interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) para receber atualizações sobre o status da indexação.

### <a name="notifications-queue"></a>Fila de notificações

Você precisa monitorar e enfileirar todas as alterações em seu armazenamento de dados para enviar ao indexador como uma notificação. Quantas notificações você coloca na fila e com que frequência elas são enviadas ao indexador depende de sua circunstância. Talvez você envie um lote de notificações para cada *n* números de alterações ou após um intervalo de tempo *t* ou uma combinação dos dois.

O indexador espera que as notificações sejam fornecidas em uma matriz de estruturas de [**\_ \_ alteração de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) , portanto, você pode optar por armazenar as informações de alteração de forma semelhante. No entanto, você também precisa ser capaz de corresponder as notificações enviadas com as confirmações e as atualizações retornadas pelo indexador. Talvez você também queira ser capaz de detectar quanto tempo leva para receber confirmações, para que você possa decidir se/quando reenviar notificações.

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Para acessar essa interface, primeiro você cria uma instância de um objeto [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) para obter acesso a um objeto [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . A partir desse objeto **ISearchCatalogManager** , você cria uma instância de um objeto [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) e notifica o indexador das alterações de dados com uma chamada para o método **onitems** .

Na chamada para esse método, você inclui o número de alterações que estão sendo relatadas e uma matriz de estruturas de [**\_ \_ alteração de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) . Você obtém de volta uma matriz de DocIds atribuídos ao indexador que representam cada alteração, bem como uma matriz de códigos de conclusão de RH que indica se cada URL foi aceita para indexação. Essa é sua confirmação do indexador de que recebeu suas notificações e está se preparando para indexar os itens.

Desse ponto em diante, o indexador envia atualizações usando a interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) .

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

Para obter atualizações sobre o status de seus itens e do catálogo, você deve registrar sua interface [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) com o indexador para que ele possa enviar retornos de chamada. Cada atualização enviada usando [**ISearchNotifyInlineSite:: OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) identifica os itens por DocId, o status de cada item ([**\_ status de \_ indexação \_ de item de pesquisa**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) e a fase de indexação ([**\_ \_ fase de indexação de pesquisa**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)) em que os itens estão.

Você não só recebe atualizações sobre o status de cada item, conforme descrito anteriormente, você também obtém informações importantes sobre o status do próprio catálogo. o serviço de pesquisa Windows pode ser interrompido ou reiniciado pelo usuário final, por um aplicativo de terceiros ou por alguma outra falha. Quando isso acontece, você precisa de uma maneira de determinar quais notificações enviar por push para o indexador.

o método [**ISearchNotifyInlineSite:: OnCatalogStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) , chamado pelo serviço de pesquisa Windows, informa os clientes sobre o status do catálogo usando os parâmetros descritos na tabela a seguir.



| Parâmetro                 | Descrição                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | Um GUID que representa a redefinição do catálogo. Se esse GUID for alterado, todas as notificações deverão ser reenviadas.                                                        |
| guidCheckPointSignature   | Um GUID que representa o último ponto de verificação restaurado. Se esse GUID for alterado, todas as notificações acumuladas desde o último ponto de verificação salvo deverão ser reenviadas. |
| dwLastCheckPointNumber    | Um número que indica o último ponto de verificação salvo.                                                                                                        |



 

 

Quando ocorre um ponto de verificação de catálogo, o serviço de pesquisa atualiza o *dwLastCheckPointNumber* e todas as notificações enviadas antes desse ponto de verificação são seguras e recuperáveis no caso de uma falha de serviço. Os provedores de notificações precisam rastrear apenas as notificações enviadas entre pontos de verificação e reenviar em caso de uma restauração ou redefinição de catálogo.

Se ocorrer uma restauração do catálogo, o serviço de pesquisa reverterá o catálogo para o último ponto de verificação salvo e atualizará o *guidCheckPointSignature*. Nessa situação, os provedores de notificações devem enviar por push todas as notificações acumuladas desde o ponto de verificação salvo mais recente, conforme identificado pelo *dwLastCheckPointNumber*.

Se uma redefinição de catálogo deve ocorrer, o serviço de pesquisa redefine todo o catálogo e atualiza o *guidCatalogResetSignature*. O provedor de notificações deve reenviar todo o escopo do rastreamento novamente.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
-   Para obter visões gerais do Gerenciador de catálogo e do CSM (Gerenciador de pesquisa de catálogo), consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).
-   Para obter informações sobre como criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Noções básicas sobre manipuladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Adicionando ícones e menus de contexto](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemplo de código: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Criando um conector de pesquisa para um manipulador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuração de manipuladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
