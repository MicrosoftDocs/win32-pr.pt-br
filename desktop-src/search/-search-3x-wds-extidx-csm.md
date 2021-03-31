---
description: O Gerenciador de escopo de rastreamento (CSM) é um conjunto de interfaces que fornece métodos para informar o mecanismo de pesquisa do Windows sobre os contêineres a serem rastreados e os itens sob esses contêineres para incluir ou excluir no catálogo.
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: Usando o Gerenciador de escopo de rastreamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef79c9e5a2a4b1dda97bf8a8be7bbaa35d5ecd2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090102"
---
# <a name="using-the-crawl-scope-manager"></a>Usando o Gerenciador de escopo de rastreamento

O Gerenciador de escopo de rastreamento (CSM) é um conjunto de interfaces que fornece métodos para informar o mecanismo de pesquisa do Windows sobre os contêineres a serem rastreados e os itens sob esses contêineres para incluir ou excluir no catálogo. Os desenvolvedores podem usar o CSM para definir um escopo de rastreamento programaticamente para um novo armazenamento de dados ou manipulador de protocolo. Os administradores podem usar o CSM para exibir os índices de todos os usuários, raízes de pesquisa e regras de escopo.

Esta seção é organizada da seguinte maneira:

-   [O que é o Gerenciador de escopo de rastreamento?](#what-is-the-crawl-scope-manager)
-   [Raízes de pesquisa e regras de escopo](#search-roots-and-scope-rules)
    -   [Raízes de pesquisa](#search-roots-and-scope-rules)
    -   [Regras de escopo](#scope-rules)
-   [Políticas de grupo com suporte pelo Gerenciador de escopo de rastreamento](#group-policies-supported-by-the-crawl-scope-manager)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>O que é o Gerenciador de escopo de rastreamento?

Para entender o Gerenciador de escopo de rastreamento, você deve entender os seguintes termos:

-   Um *escopo de rastreamento* é um conjunto de URLs que apontam para repositórios de dados ou contêineres (armazenamentos de dados de email, bancos de dados, compartilhamentos de arquivos de rede e assim por diante) que o indexador rastreia para indexar itens. Para um armazenamento de dados hierárquico, o escopo do rastreamento pode incluir uma URL pai, mas excluir uma URL filho e vice-versa. Os itens dentro do escopo de rastreamento são indexados; os itens fora do escopo do rastreamento são ignorados.
-   Uma *raiz de pesquisa* é a URL de nível superior que identifica um armazenamento de contêiner ou de dados associado a um manipulador de protocolo específico. Raízes de pesquisa podem identificar locais específicos de um usuário, que estão em um computador remoto ou que correspondem a um padrão de curinga. Ao adicionar um novo armazenamento de dados ou manipulador de protocolo, você também deve adicionar uma raiz de pesquisa ao escopo do rastreamento.
-   Uma *regra de escopo* é uma regra que inclui ou exclui URLs em uma raiz de pesquisa de serem rastreadas e indexadas. Por exemplo, suponha que você queira que tudo dentro da pasta ProjectFiles seja indexado, exceto pelos protótipos de subpasta. Você precisaria de uma regra de inclusão para file:///C: \\ WorkteamA \\ ProjectFiles \\ e uma regra de exclusão para os \\ protótipos file:///C: WorkteamA \\ ProjectFiles \\ \\ .

O **Gerenciador de escopo de rastreamento (CSM)** é um conjunto de APIs que permite adicionar, remover e enumerar raízes de pesquisa e regras de escopo para o indexador do Windows Search. Quando desejar que o indexador comece a rastrear um novo contêiner, você poderá usar o CSM para definir as raízes de pesquisa e as regras de escopo dos caminhos nas raízes de pesquisa. Por exemplo, se você instalar um novo manipulador de protocolo, poderá criar uma raiz de pesquisa e adicionar uma ou mais regras de inclusão; em seguida, o indexador pode iniciar um rastreamento para a indexação inicial. O CSM oferece as seguintes interfaces para ajudá-lo a fazer isso programaticamente.

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

Embora você possa usar as APIs CSM para definir um escopo de rastreamento programaticamente, o CSM foi projetado para dar suporte a usuários finais também. Por exemplo, suponha que você tenha desenvolvido um manipulador de protocolo para um novo armazenamento de dados e queira permitir que os usuários ou administradores gerenciem quais caminhos devem ser indexados. Você pode usar o Gerenciador de escopo de rastreamento para definir uma ou mais raízes de pesquisa (por exemplo, file:///C: \\ MyContainer \\ ) e a interface do usuário do Windows Search para definir opções de indexação exibirá cada raiz de pesquisa com uma caixa de seleção. Os usuários podem incluir ou excluir o caminho ou os filhos desse caminho.

## <a name="search-roots-and-scope-rules"></a>Raízes de pesquisa e regras de escopo

As raízes de pesquisa e as regras de escopo juntas definem um conjunto de trabalho de URLs que compõem o escopo de rastreamento do indexador.

### <a name="search-roots"></a>Raízes de pesquisa

Definir uma raiz de pesquisa não especifica quais partes desse armazenamento devem ser indexadas; Ele simplesmente sinaliza que um repositório de conteúdo existe e está associado a um manipulador de protocolo registrado. A sintaxe de uma raiz de pesquisa inclui um protocolo, um site ou um identificador de segurança de usuário e um caminho para os locais a serem rastreados.

Você deve criar novas raízes de pesquisa quando:

-   Instalar um manipulador de protocolo ou
-   Deseja indexar um novo armazenamento de dados

AND

-   esse armazenamento de dados ainda não está no escopo de rastreamento do indexador.

Consulte [Gerenciando raízes de pesquisa](-search-3x-wds-extidx-csm-searchroots.md) para obter instruções sobre como adicionar, remover e enumerar raízes de pesquisa.

### <a name="scope-rules"></a>Regras de escopo

As regras de escopo incluem ou excluem URLs em uma raiz de pesquisa de serem rastreadas e indexadas. As regras de escopo podem ser definidas por usuários finais, por política de grupo ou por desenvolvedores de terceiros. Você deve definir regras de escopo programaticamente ao definir uma nova raiz de pesquisa. Suas raízes de pesquisa e regras de escopo incluem o escopo de rastreamento padrão para o armazenamento de dados e o manipulador de protocolo.

> [!Note]  
> Os usuários com acesso ao painel de controle podem modificar o escopo de rastreamento padrão. Portanto, qualquer aplicativo que ofereça gerenciamento de escopo sempre deve obter as regras diretamente do CSM usando os métodos de enumeração em vez de depender de sua própria cópia salva das regras do usuário.

 

Consulte [Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md) para obter instruções sobre como adicionar, remover, reverter e enumerar regras de escopo.

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>Políticas de grupo com suporte pelo Gerenciador de escopo de rastreamento

Os administradores do sistema podem definir escopos de rastreamento em suas organizações usando políticas de grupo. Essas regras de diretiva de grupo também podem atuar como regras padrão, que os usuários podem substituir. Por exemplo, você pode ter um conjunto de diretórios indexados para um grupo de usuários e um conjunto diferente para outro grupo de usuários, permitindo que os usuários desmarquem esses padrões. As regras de política de grupo também podem atuar como regras de exclusão forçada que os usuários não podem substituir, impedindo que determinados usuários indexem determinados compartilhamentos de rede, por exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando raízes de pesquisa](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[O processo de indexação](-search-indexing-process-overview.md)
</dt> </dl>

 

 
