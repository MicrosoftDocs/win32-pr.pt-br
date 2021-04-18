---
description: As interfaces ISearchCatalogManager e ISearchCatalogManager2 fornecem métodos para gerenciar um catálogo de pesquisa, como a causa da reindexação ou da configuração de tempos limite.
ms.assetid: 8dad7012-d610-4398-8e86-cd319db8c360
title: Usando o Gerenciador de catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1295cc9cc76fb334b4687b876fa1959a22e33235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789992"
---
# <a name="using-the-catalog-manager"></a>Usando o Gerenciador de catálogo

As interfaces [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2) fornecem métodos para gerenciar um catálogo de pesquisa, como a causa da reindexação ou da configuração de tempos limite. Embora o Windows Search use atualmente apenas um catálogo, essa interface foi projetada para fornecer a você maior controle para o gerenciamento de vários catálogos de forma independente. A interface gerencia o catálogo das seguintes maneiras:

- Acesso a outras interfaces — recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador de escopo de rastreamento, notificações de alteração de dados e a interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) .
- Conteúdo do catálogo — garantindo que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente, forçando uma reindexação de todo ou parte do catálogo ou redefinindo o catálogo inteiro.
- Propriedades do catálogo — definir propriedades que determinam como o catálogo gerencia os tempos limite ao se conectar a manipuladores de protocolo e como as marcas de diacríticos são tratadas em pesquisas.
- Status do catálogo — obtendo informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.

Este tópico é organizado da seguinte maneira:

- [Acessando interfaces relacionadas](#accessing-related-interfaces)
- [Gerenciando o conteúdo do catálogo](#managing-the-catalog-contents)
- [Gerenciando o status do catálogo](#managing-catalog-status)
- [Gerenciando Propriedades de catálogo](#managing-catalog-properties)
- [Executando em modo elevado](#running-in-elevated-mode)
- [Tópicos relacionados](#related-topics)

## <a name="accessing-related-interfaces"></a>Acessando interfaces relacionadas

Algumas interfaces úteis na plataforma de pesquisa do Windows exigem uma instância do Gerenciador de catálogo antes que possam ser usadas. Para criar um Gerenciador de catálogo para um catálogo especificado, chame o método [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) . Os métodos do Gerenciador de catálogo podem ser usados para instanciar e retornar interfaces baseadas no catálogo especificado.

| Método                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)                               | Obtém uma instância da interface [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) para o catálogo atual, para permitir que você crie consultas facilmente.                                                                                                                                                                                                                         |
| [**GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager)                   | Obtém uma instância de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para este catálogo de pesquisa, para permitir que os desenvolvedores modifiquem o escopo de rastreamento do indexador do Windows Search.                                                                                                                                                                                    |
| [**GetItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink)                     | Obtém uma instância da interface [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) , que os aplicativos cliente usam para notificar o indexador de alterações quando o cliente desejar informações de status de indexação sobre o item para dar suporte a notificações gerenciadas por provedor. Consulte [notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md) para obter mais informações. |
| [**GetPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink) | Obtém uma instância de [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink), que os aplicativos cliente usam para notificar o indexador de alterações quando o cliente não deseja informações de status de indexação (notificações gerenciadas pelo indexador). Consulte [notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md) para obter mais informações.            |

## <a name="managing-the-catalog-contents"></a>Gerenciando o conteúdo do catálogo

Há duas tarefas principais envolvidas no gerenciamento do catálogo: reindexar todas ou algumas das URLs no escopo de rastreamento do indexador e redefinir todo o catálogo subjacente. Quando você reindexar URLs, os dados antigos permanecerão no catálogo até ou, a menos que sejam substituídos por novos dados. Quando você redefine o catálogo, todo o catálogo é recriado e todas as URLs no escopo do rastreamento são reindexadas. Esse processo pode levar muito tempo e deve ser usado apenas como último recurso para resolver problemas, como um índice possivelmente corrompido.

Quando você instala um novo aplicativo, manipulador de protocolo ou filtro, o aplicativo de instalação deve adicionar seu diretório ou raiz ao escopo de rastreamento para garantir que o indexador inclua o local dos dados desse aplicativo. Se os dados não aparecerem no catálogo depois que o indexador tiver rastreado seu escopo de rastreamento, primeiro verifique se o local dos dados está incluído no escopo do rastreamento. Você pode adicioná-lo usando a interface do usuário para as opções de pesquisa do Windows ou o [Gerenciador de escopo do rastreamento](-search-3x-wds-extidx-csm.md). Se o local parecer estar no escopo de rastreamento, você poderá forçar manualmente uma reindexação de todas as URLs no escopo de rastreamento do indexador ou um subconjunto, usando os métodos a seguir da interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .

| Método de reindexação                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISearchCatalogManager:: reindexar**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindex)                                                                                                                                                   | Indexa novamente todas as URLs no catálogo. As informações antigas permanecerão até que sejam substituídas por novas informações.                                                                                                                                                         |
| [**ISearchCatalogManager::ReindexMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls)<br/> [**ISearchCatalogManager::ReindexSearchRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot)<br/> | Reindexa as URLs que correspondem ao padrão ou começam em uma raiz específica (por exemplo, file:///C: \\ nome_da_pasta \\ subfoldername \\ ). Isso é útil para rerastrear tudo em um determinado diretório ou com uma extensão específica, como quando um aplicativo é instalado. |
| [**PrioritizeMatchingURLs**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls)                                                                                                                                           | Instrui o indexador a priorizar itens de indexação com URLs que correspondem a um padrão especificado ao concluir outras tarefas de indexação.                                                                                                                                    |

**Redefinindo o índice.** Você pode redefinir o índice inteiro com uma chamada para [**ISearchCatalogManager:: Reset**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-reset). Isso redefine o catálogo subjacente recriando os bancos de dados e executando um índice completo de todas as URLs no escopo de rastreamento. Esse processo pode levar muito tempo e deve ser usado apenas como último recurso para resolver problemas, como um índice possivelmente corrompido.

> [!IMPORTANT]
> Devido à lentidão na indexação que esses métodos podem causar, eles devem ser usados com cuidado quando você estiver tentando identificar problemas de indexação ou de catálogo. Primeiro, verifique se as raízes de pesquisa e as regras de escopo foram adicionadas no Gerenciador de escopo de rastreamento e certifique-se de que o (atributo de arquivo sem conteúdo indexado) esteja definido corretamente para arquivos e pastas. Se você confirmou que eles estão corretos, tente ReindexSearchRoot primeiro e reindexar por último. Se nenhum desses trabalhos, tente redefinir como último recurso.

Para obter informações relacionadas, consulte [notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md)e [consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

## <a name="managing-catalog-status"></a>Gerenciando o status do catálogo

O Gerenciador de catálogo pode ser usado para obter o status do catálogo para aplicativos que desejam personalizar como o catálogo é gerenciado (por exemplo, um aplicativo de monitoramento "status do catálogo" personalizado). Mas o Gerenciador de catálogo normalmente não é necessário para a maioria dos cenários de desenvolvimento relacionados à pesquisa. Usos comuns seriam para um aplicativo de monitoramento de "status do catálogo" ou um aplicativo estilo do painel de controle.

A tabela a seguir descreve os métodos de ISearchCatalogManager usados para gerenciar o status do catálogo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed"><strong>URLBeingIndexed</strong></a></td>
<td>Obtém a URL que está sendo indexada no momento. Esse método seria útil se você estava tentando identificar se o indexador estava &quot; preso &quot; em um item.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitems"><strong>NumberOfItems</strong></a></td>
<td>Obtém o número de itens no catálogo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex"><strong>NumberOfItemsToIndex</strong></a></td>
<td>Recupera as seguintes informações sobre os itens a serem indexados:
<ul>
<li>plIncrementalCount-o número de itens a serem indexados no próximo índice incremental</li>
<li>plNotificationQueue-o número de itens na fila de notificação. Essas informações seriam úteis para um aplicativo de notificação que precisava verificar se o indexador está recebendo as notificações que o aplicativo está enviando.</li>
<li>plHighPriorityQueue-o número de itens na fila de alta prioridade. Os itens no plHighPriorityQueue são indexados primeiro.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus"><strong>GetCatalogStatus</strong></a></td>
<td>Obtém o status do catálogo e retorna um valor de enumeração que fornece o status atual. Estes são os Estados de catálogo possíveis:
<ul>
<li>Ocioso: nenhuma indexação é necessária.</li>
<li>Em pausa: a indexação está em pausa (devido à baixa bateria ou alta utilização da CPU, por exemplo).</li>
<li>Recuperando: a indexação está sendo recuperada.</li>
<li>Rastreamento completo: o indexador está executando um rastreamento completo do escopo do rastreamento.</li>
<li>Rastreamento incremental: o indexador está executando um rastreamento incremental.</li>
<li>Processando notificações: o indexador está processando notificações.</li>
<li>Desligando: o indexador está sendo desligado.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_name"><strong>get_Name</strong></a></td>
<td>Obtém o nome do catálogo atual especificado no método <a href="/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog"><strong>ISearchManager:: getCatalog</strong></a> . Atualmente, o único catálogo com suporte é SystemIndex.</td>
</tr>
</tbody>
</table>

## <a name="managing-catalog-properties"></a>Gerenciando Propriedades de catálogo

Há três propriedades de catálogo que você pode gerenciar com o Gerenciador de catálogo:

- **Sensibilidade de sinais diacríticos.** Diacríticos são marcas de acentos adicionadas a letras para significar o significado ou a pronúncia de um texto. Essa propriedade determina se o catálogo é sensível a diacríticos e é importante quando você ou seus usuários pesquisam e indexam texto em vários idiomas. Por exemplo, com essa propriedade definida como **false**, o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.
- **Tempos limite de conexão.** Essa propriedade representa a quantidade de tempo de espera por uma resposta de conexão de um servidor ou armazenamento de dados, conforme representado em uma estrutura de [**\_ informações de tempo limite**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Você pode usar essa propriedade para ajustar o Windows Search.
- **Tempos limite de dados** Essa propriedade representa a quantidade de tempo de espera para uma transação de dados entre o indexador e um manipulador de protocolo ou filtro, conforme representado em uma estrutura de [**\_ informações de tempo limite**](/windows/desktop/api/Searchapi/ns-searchapi-timeout_info) . Se esse tempo tiver decorrido, o processo do daemon de filtro será encerrado para evitar o deadlock e outros problemas de recurso.

As duas últimas propriedades são destinadas principalmente para uso futuro. Cada uma dessas propriedades tem `get` `put` métodos e.

| Método                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity) /<br/> [**colocar \_ DiacriticSensitivity**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity)<br/> | TRUE se o catálogo deve diferenciar palavras com sinais diacríticos. **False** se o catálogo deve ignorar diacríticos. A alteração dessa propriedade requer a recriação do índice porque as chaves do índice podem se tornar inválidas.                       |
| [**obter \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout) /<br/> [**colocar \_ ConnectTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout)<br/>                         | O tempo, em segundos, que o indexador deve aguardar uma resposta de conexão de um servidor ou armazenamento de dados. Definir isso muito alto pode causar atrasos se muitos sites não responderem. Configurá-lo muito baixo pode resultar em alguns sites que não estão sendo rastreados. |
| [**obter \_ data limite**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout) /<br/> [**colocar \_ DataTimeout**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout)<br/>                                     | O tempo, em segundos, que o indexador deve esperar por uma transação de dados.                                                                                                                                                                      |

## <a name="running-in-elevated-mode"></a>Executando em modo elevado

Qualquer chamada de método que atualize o SystemIndex exige que seu aplicativo seja executado com privilégios elevados. Caso contrário, seu aplicativo falhará com um erro de acesso negado.

## <a name="related-topics"></a>Tópicos relacionados


[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)

[Interfaces para gerenciar o índice](interfaces-for-managing-the-index.md)

[Usando o Gerenciador de pesquisa](-search-3x-wds-mngidx-searchmanager.md)

[Usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md)
