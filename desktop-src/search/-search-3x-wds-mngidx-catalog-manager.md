---
description: As interfaces ISearchCatalogManager e ISearchCatalogManager2 fornecem métodos para gerenciar um catálogo de pesquisa, como a re indexação ou a definição de tempos-máximos.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Usando o Gerenciador de Catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deffc748c504b056e9d3f92dc8dcb127b835bec6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472322"
---
# <a name="using-the-catalog-manager"></a>Usando o Gerenciador de Catálogo

As interfaces [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) fornecem métodos para gerenciar um catálogo de pesquisa, como a re indexação ou a definição de tempos-máximos. Embora Windows Search atualmente use apenas um catálogo, essa interface foi projetada para dar a você maior controle para gerenciar vários catálogos de forma independente. A interface gerencia o catálogo das seguintes maneiras:

- Acesso a outras interfaces – recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador do Escopo de Rastreamento, notificações de alteração de dados e a interface [**ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)
- Conteúdo do catálogo – garantir que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente forçando uma nova indexação de todo ou parte do catálogo ou redefinindo todo o catálogo.
- Propriedades do catálogo – definindo propriedades que determinam como o catálogo gerencia tempos-tempos ao se conectar a manipuladores de protocolo e como as marcas diacríticas são tratadas em pesquisas.
- Status do catálogo – obter informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.

Este tópico é organizado da seguinte forma:

- [Acessando interfaces relacionadas](#accessing-related-interfaces)
- [Gerenciando o conteúdo do catálogo](#managing-the-catalog-contents)
- [Gerenciando o status do catálogo](#managing-catalog-status)
- [Gerenciando propriedades do catálogo](#managing-catalog-properties)
- [Em execução no modo elevado](#running-in-elevated-mode)
- [Tópicos relacionados](#related-topics)

## <a name="accessing-related-interfaces"></a>Acessando interfaces relacionadas

Algumas interfaces úteis na plataforma Windows Search exigem uma instância do Gerenciador de Catálogo antes que possam ser usadas. Para criar um Gerenciador de Catálogo para um catálogo especificado, chame o [**método ISearchManager::GetCatalog.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) Os métodos do Gerenciador de Catálogo podem ser usados para insinciar e retornar interfaces baseadas no catálogo especificado.

| Método                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Obtém uma instância da interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para o catálogo atual, para permitir que você crie consultas facilmente.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Obtém uma instância de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para este catálogo de pesquisa, para permitir que os desenvolvedores modifiquem o escopo de rastreamento do indexador Windows Search.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Obtém uma instância da interface [**ISearchItemsChangedSink,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) que os aplicativos cliente usam para notificar o indexador de alterações quando o cliente deseja indexar informações de status sobre o item para dar suporte a notificações gerenciadas pelo provedor. Consulte [Notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md) para obter mais informações. |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Obtém uma instância de [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), que os aplicativos cliente usam para notificar o indexador de alterações quando o cliente não deseja informações de status de indexação (notificações gerenciadas pelo indexador). Consulte [Notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md) para obter mais informações.            |

## <a name="managing-the-catalog-contents"></a>Gerenciando o conteúdo do catálogo

Há duas tarefas principais envolvidas no gerenciamento do catálogo: indexar novamente todas ou algumas das URLs no escopo de rastreamento do indexador e redefinir todo o catálogo subjacente. Quando você re indexa URLs, os dados antigos permanecem no catálogo até ou a menos que eles são substituídos por novos dados. Quando você redefine o catálogo, todo o catálogo é reconstruído e todas as URLs no escopo do rastreamento são indexadas novamente. Esse processo pode levar muito tempo e deve ser usado apenas como último recurso para resolver problemas como um índice possivelmente corrompido.

Quando você instala um novo aplicativo, manipulador de protocolo ou filtro, o aplicativo de instalação deve adicionar seu diretório ou raiz ao escopo de rastreamento para garantir que o indexador inclua o local dos dados desse aplicativo. Se os dados não aparecerem no catálogo depois que o indexador tiver rastreado seu escopo de rastreamento, primeiro você deverá garantir que o local dos dados seja incluído no escopo de rastreamento. Você pode adicioná-lo usando a interface do usuário para Windows Search ou o [Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md). Se o local parecer estar no escopo do rastreamento, você poderá forçar manualmente uma nova indexação de todas as URLs no escopo de rastreamento do indexador ou em um subconjunto, usando os métodos a seguir da interface [**ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

| Método de re indexação                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager::Reindex**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Re indexa todas as URLs no catálogo. As informações antigas permanecerão até que ela seja substituída por novas informações.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Indexa as URLs que corresponderem ao padrão ou começam em uma raiz específica (por exemplo, file:///C: \\ \\ NomedaPasta de \\ Pastanome da pasta). Isso é útil para reeplicação de tudo em um diretório específico ou com uma extensão específica, como quando um aplicativo é instalado. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Instrui o indexador a priorizar itens de indexação com URLs que corresponderem a um padrão especificado em vez de concluir outras tarefas de indexação.                                                                                                                                    |

**Redefinindo o índice.** Você pode redefinir todo o índice com uma chamada para [**ISearchCatalogManager::Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Isso redefine o catálogo subjacente recriando os bancos de dados e executando um índice completo de todas as URLs no escopo de rastreamento. Esse processo pode levar muito tempo e deve ser usado apenas como último recurso para resolver problemas como um índice possivelmente corrompido.

> [!IMPORTANT]
> Devido à lentidão na indexação que esses métodos podem causar, eles devem ser usados com cuidado quando você estiver tentando identificar problemas de indexação ou catálogo. Primeiro, certifique-se de que suas raízes de pesquisa e regras de escopo sejam adicionadas no Gerenciador do Escopo de Rastreamento e, em seguida, certifique-se de que o bit FANCI (Atributo de Arquivo Não Indexado) está definido corretamente para arquivos e pastas. Se você confirmou que eles estão corretos, tente ReindexSearchRoot primeiro e Reindex por último. Se nenhum desses trabalhos funcionar, tente Redefinir como último recurso.

Para obter informações relacionadas, consulte [Notificando](-search-3x-wds-notifyingofchanges.md)o índice de alterações e Consultando o [índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Gerenciando o status do catálogo

O Gerenciador de Catálogo pode ser usado para obter o status do catálogo para aplicativos que querem personalizar como o catálogo é gerenciado (por exemplo, um aplicativo de monitoramento personalizado de "Status do Catálogo"). Mas o Gerenciador de Catálogo normalmente não é necessário para a maioria dos cenários de desenvolvimento relacionados à pesquisa. Usos comuns seriam para um aplicativo de monitoramento de "Status do Catálogo" ou um Painel de Controle de estilo único.

A tabela a seguir descreve os métodos de ISearchCatalogManager usados para gerenciar o status do catálogo.


| Método | Descrição | 
|--------|-------------|
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a> | Obtém a URL que está sendo indexada no momento. Esse método seria útil se você estivesse tentando identificar se o indexador estava "preso" em um item. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a> | Obtém o número de itens no catálogo. | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a> | Recupera as seguintes informações sobre os itens a serem indexados:<ul><li>plIncrementalCount – o número de itens a serem indexados no próximo índice incremental</li><li>plNotificationQueue – o número de itens na fila de notificação. Essas informações seriam úteis para um aplicativo de notificação que precisava verificar se o indexador está recebendo as notificações que o aplicativo está enviando.</li><li>plHighPriorityQueue – o número de itens na fila de alta prioridade. Os itens no plHighPriorityQueue são indexados primeiro.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a> | Obtém o status do catálogo e retorna um valor de enumeração que fornece o status atual. Veja a seguir os possíveis estados do catálogo:<ul><li>Ocioso: nenhuma indexação é necessária.</li><li>Pausado: a indexação está em pausa (devido à bateria baixa ou ao alto uso da CPU, por exemplo).</li><li>Recuperação: a indexação está recuperando.</li><li>Rastreamento completo: o indexador está executando um rastreamento completo do escopo de rastreamento.</li><li>Rastreamento incremental: o indexador está executando um rastreamento incremental.</li><li>Notificações de processamento: o indexador está processando notificações.</li><li>Desligando: o indexador está sendo desligado.</li></ul> | 
| <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a> | Obtém o nome do catálogo atual especificado no <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>método ISearchManager::GetCatalog.</strong></a> Atualmente, o único catálogo com suporte é SystemIndex. | 


## <a name="managing-catalog-properties"></a>Gerenciando propriedades do catálogo

Há três propriedades de catálogo que você pode gerenciar com o Gerenciador de Catálogo:

- **Sensibilidade diacrítica.** Diacríticas são marcas de destaque adicionadas às letras para significar o significado ou a pronúncia de uma palavra. Essa propriedade determina se o catálogo é sensível a diacríticas e é importante quando você ou seus usuários pesquisam e indexam texto em vários idiomas. Por exemplo, com essa propriedade definida como **FALSE,** o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.
- **Tempos de conexão.** Essa propriedade representa a quantidade de tempo de espera por uma resposta de conexão de um servidor ou armazenamento de dados, conforme representado em uma estrutura [**TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) Você pode usar essa propriedade para ajustar a Windows Search.
- **Tempos de vida dos dados** Essa propriedade representa a quantidade de tempo de espera por uma transação de dados entre o indexador e um manipulador de protocolo ou filtro, conforme representado em uma estrutura [**TIMEOUT \_ INFO.**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) Se esse tempo tiver decorrido, o processo do Daemon de Filtro será encerrado para evitar deadlock e outros problemas de recurso.

As duas últimas propriedades são destinadas principalmente para uso futuro. Cada uma dessas propriedades tem `get` métodos `put` e .

| Método                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**put \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE se o catálogo deve diferenciar palavras com diacríticas. **FALSE** se o catálogo deve ignorar diacríticas. Alterar essa propriedade requer a recriação do índice porque as chaves do índice podem se tornar inválidas.                       |
| [**get \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**put \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | O tempo, em segundos, em que o indexador deve aguardar uma resposta de conexão de um servidor ou armazenamento de dados. Definir isso muito alto poderá causar atrasos se muitos sites não responderem. Defini-lo muito baixo pode fazer com que alguns sites não possam ser rastreados. |
| [**get \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**put \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | O tempo, em segundos, que o indexador deve aguardar por uma transação de dados.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Em execução no modo elevado

Todas as chamadas de método que atualizem o SystemIndex exigem que seu aplicativo seja executado com elevação. Caso contrário, seu aplicativo falhará com um erro acesso negado.

## <a name="related-topics"></a>Tópicos relacionados


[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para gerenciar o índice](interfaces-for-managing-the-index.md)

[Usando o Gerenciador de Pesquisa](-search-3x-wds-mngidx-searchmanager.md)

[Usando o Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md)
