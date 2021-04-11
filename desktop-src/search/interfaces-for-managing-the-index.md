---
description: 'O Windows Search permite que você gerencie o índice do Windows Search com três componentes principais: Gerenciador de pesquisa, Gerenciador de catálogo e Gerenciador de escopo de rastreamento.'
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para gerenciar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7191fbdb4e83c9e3f1460b96123901b5f277b41a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164328"
---
# <a name="interfaces-for-managing-the-index"></a>Interfaces para gerenciar o índice

O Windows Search permite que você gerencie o índice do Windows Search com três componentes principais: Gerenciador de pesquisa, Gerenciador de catálogo e Gerenciador de escopo de rastreamento. Algumas dessas interfaces de gerenciamento podem ser usadas com privilégios de usuário padrão, mas as que alteram o estado do índice exigem privilégios administrativos.

## <a name="about-the-interfaces-for-managing-the-index"></a>Sobre as interfaces para gerenciar o índice

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Interfaces</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gerenciador de pesquisa</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>Fornece métodos para recuperar e definir informações sobre o Windows Search:
<ul>
<li>Obter uma instância do Gerenciador de catálogo para um catálogo específico.</li>
<li>Obter ou definir informações de proxy.</li>
<li>Obtendo informações de versão sobre o mecanismo de pesquisa do Windows.</li>
</ul>
Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">usando o Gerenciador de pesquisa</a>.<br/></td>
</tr>
<tr class="even">
<td>Gerenciador de catálogos</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Fornece métodos para gerenciar um catálogo de pesquisa individual, como causar uma nova indexação ou definir tempos limite. Essa interface gerencia o catálogo em quatro áreas:
<ul>
<li>Conteúdo do catálogo – garantindo que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente, forçando uma reindexação de todo ou parte do catálogo ou redefinindo o catálogo inteiro.</li>
<li>Propriedades do catálogo – definir propriedades que determinam como o catálogo gerencia os tempos limite ao se conectar a manipuladores de protocolo e como as marcas de diacríticos são tratadas em pesquisas.</li>
<li>Status do catálogo-obtendo informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.</li>
<li>Acesso a outras interfaces – recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador de escopo de rastreamento, notificações de alteração de dados e a interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</li>
</ul>
Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-catalog-manager.md">usando o Gerenciador de catálogo</a>.<br/></td>
</tr>
<tr class="odd">
<td>Gerenciador de escopo de rastreamento</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>Fornece métodos para informar o mecanismo de pesquisa sobre contêineres para rastreamento ou inspeção e itens sob esses contêineres para incluir ou excluir no índice. Você também pode consultar o Gerenciador de escopo de rastreamento para ver se uma URL específica está no escopo do rastreamento. Para obter mais informações, consulte <a href="-search-3x-wds-extidx-csm.md">usando o Gerenciador de escopo de rastreamento</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Tópicos relacionados

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)

[Usando o Gerenciador de pesquisa](-search-3x-wds-mngidx-searchmanager.md)

[Usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md)

[Usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md)
