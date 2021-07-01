---
description: Saiba como Windows Search permite gerenciar o índice Windows Search com o Gerenciador de Pesquisa, o Gerenciador de Catálogos e Gerenciador do Escopo de Rastreamento.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces para gerenciar o índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120011"
---
# <a name="interfaces-for-managing-the-index"></a>Interfaces para gerenciar o índice

Windows Search permite gerenciar o índice Windows Search com três componentes principais: Gerenciador de Pesquisa, Gerenciador de Catálogos e Gerenciador do Escopo de Rastreamento. Algumas dessas interfaces de gerenciamento podem ser usadas com privilégios de usuário padrão, mas aquelas que alteram o estado do índice exigem privilégios administrativos.

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
<td>Gerenciador de Pesquisa</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>Fornece métodos para recuperar e definir informações sobre Windows Search:
<ul>
<li>Obter uma instância do Gerenciador de Catálogo para um catálogo específico.</li>
<li>Obter ou definir informações de proxy.</li>
<li>Obter informações de versão sobre o Windows Search de dados.</li>
</ul>
Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-searchmanager.md">Usando o Gerenciador de Pesquisa</a>.<br/></td>
</tr>
<tr class="even">
<td>Gerenciador de Catálogo</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>Fornece métodos para gerenciar um catálogo de pesquisa individual, como causar uma nova indexação ou definir tempos-máximos. Essa interface gerencia o catálogo em quatro áreas:
<ul>
<li>Conteúdo do catálogo – garantir que novos dados sejam indexados e que outros aplicativos e componentes funcionem corretamente forçando uma nova indexação de todo ou parte do catálogo ou redefinindo todo o catálogo.</li>
<li>Propriedades do catálogo – definindo propriedades que determinam como o catálogo gerencia tempos-tempos ao se conectar a manipuladores de protocolo e como as marcas diacríticas são tratadas em pesquisas.</li>
<li>Status do catálogo – obter informações sobre o catálogo, incluindo status, tamanho e estado da atividade atual.</li>
<li>Acesso a outras interfaces – recuperando outras interfaces relacionadas à pesquisa exigidas pelo Gerenciador do Escopo de Rastreamento, notificações de alteração de dados e a interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper.</strong></a></li>
</ul>
Para obter mais informações, consulte <a href="-search-3x-wds-mngidx-catalog-manager.md">Usando o Gerenciador de Catálogo.</a><br/></td>
</tr>
<tr class="odd">
<td>Gerenciador do Escopo de Rastreamento</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>Fornece métodos para informar o mecanismo de pesquisa sobre contêineres a rastrear ou observar e itens nesses contêineres para incluir ou excluir no índice. Você também pode consultar o Gerenciador do Escopo de Rastreamento para ver se uma URL específica está no escopo do rastreamento. Para obter mais informações, <a href="-search-3x-wds-extidx-csm.md">consulte Usando o Gerenciador do Escopo de Rastreamento</a>.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Tópicos relacionados

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)

[Usando o Gerenciador de Pesquisa](-search-3x-wds-mngidx-searchmanager.md)

[Usando o Gerenciador de Catálogo](-search-3x-wds-mngidx-catalog-manager.md)

[Usando o Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md)
