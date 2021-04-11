---
description: O Gerenciador de escopo de rastreamento (CSM) permite adicionar e remover raízes de pesquisa para os armazenamentos de dados de e para o escopo de rastreamento do Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gerenciando raízes de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164344"
---
# <a name="managing-search-roots"></a>Gerenciando raízes de pesquisa

O Gerenciador de escopo de rastreamento (CSM) permite adicionar e remover raízes de pesquisa para os armazenamentos de dados de e para o escopo de rastreamento do Windows Search.

Este tópico abrange os seguintes assuntos:

-   [Sobre raízes de pesquisa](#about-search-roots)
-   [Antes de começar](#before-you-begin)
-   [Windows 7: nova API do Gerenciador de escopo de rastreamento](#windows-7-new-crawl-scope-manager-api)
-   [Adicionando raízes ao escopo de rastreamento](#adding-roots-to-the-crawl-scope)
-   [Removendo raízes do escopo de rastreamento](#removing-roots-from-the-crawl-scope)
-   [Enumerando raízes no escopo de rastreamento](#enumerating-roots-in-the-crawl-scope)
-   [Tópicos relacionados](#related-topics)

 

## <a name="about-search-roots"></a>Sobre raízes de pesquisa

Uma raiz de pesquisa define a base de um namespace de Shell em que escopos específicos podem ser incluídos ou excluídos e geralmente é o contêiner de nível mais alto em um protocolo que pode ser enumerado. Ele não especifica quais partes desse armazenamento devem ou não ser indexadas; Ele simplesmente sinaliza que um repositório de conteúdo existe e está associado a um manipulador de protocolo registrado. A sintaxe para identificar uma URL raiz de pesquisa inclui o protocolo, o identificador de segurança do repositório ou do usuário, o caminho e, opcionalmente, um item específico (como um arquivo). Os exemplos a seguir mostram duas formas da sintaxe para uma raiz de pesquisa.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



O <protocol> segmento deve ser seguido de duas (2) barras "/" ("/"), a menos que seja o protocolo file:, que requer três barras (file:///). O <site or SID> segmento representa um repositório de conteúdo ou um identificador de segurança de usuário se a raiz de pesquisa for destinada a ser específica ao usuário. O <path> segmento é um conjunto de contêineres, como diretórios ou pastas, e pode incluir o caractere curinga ' \* '. O <item> o segmento é opcional e também pode incluir o caractere curinga ' \* '. Se você não incluir um item, certifique-se de concluir o segmento de caminho com uma barra ou o indexador irá pressupor que o último subcontêiner é um item.

Por exemplo, suponha que você implementou um manipulador de protocolo (myPH) para manipular arquivos do tipo \* . myext para um aplicativo personalizado. Todos esses arquivos estarão localizados na pasta WorkteamA \\ ProjectFiles em um computador local. A raiz de pesquisa para isso pode ser assim:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Suponha que você esteja planejando incluir todos os arquivos. myext, mas nada mais desse contêiner no índice. A raiz de pesquisa para isso pode ser assim:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* . myext.

Os padrões de caractere curinga definem URLs usando o caractere curinga " \* " e são considerados um padrão em vez de uma URL, mas a terminologia geralmente é usada de forma intercambiável. Por exemplo, file:///C: os \\ \\ \* \\ dados do projecta \\ corresponderão às seguintes URLs:

-   C: \\ dados do projecta \\ **versão** \\\\
-   C: \\ dados do projecta \\ **Version2** \\\\

Mas esse padrão não corresponde a essa URL:

-   C: \\ \\ **dados \\ temporários** do projecta versão \\\\

Você deve criar novas raízes de pesquisa para contêineres que ainda não estão no escopo de rastreamento do indexador. Se o caminho C: \\ ParentScope já estiver incluído no escopo de rastreamento, você não precisará adicionar uma nova raiz de pesquisa para C: \\ ParentScope \\ ChildScope, a menos que você saiba que o escopo filho foi excluído anteriormente.

A interface do usuário para definir as opções de pesquisa do Windows exibe raízes de pesquisa para os usuários para que eles possam refinar as regras de escopo para suas pesquisas. Como parte do processo de instalação para seu manipulador de protocolo, contêiner e/ou aplicativo personalizado, você pode definir um escopo de rastreamento padrão, com regras de inclusão e exclusão. Essas regras são apresentadas aos usuários finais como locais. Os usuários podem navegar dentro dos subdiretórios de sua raiz de pesquisa predefinida e selecionar aqueles que desejam incluir nas pesquisas ou desmarcar aqueles que desejam excluir.

 

## <a name="before-you-begin"></a>Antes de começar

Antes de poder usar qualquer uma das interfaces do CSM (Gerenciador de escopo de rastreamento), você deve executar as seguintes etapas de pré-requisito:

1.  Crie o objeto **CrawlSearchManager** e obtenha sua interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
2.  Chame [**ISearchManager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) para "SystemIndex" para obter uma instância de uma interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .
3.  Chame [**ISearchCatalogManager:: GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) para obter uma instância da interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .

Depois de fazer alterações no Gerenciador de escopo de rastreamento (CSM), você deve chamar [**ISearchCrawlScopeManager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Esse método não usa parâmetros e retorna S \_ OK em caso de êxito.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: nova API do Gerenciador de escopo de rastreamento

No **Windows 7 e posterior**, o [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende a funcionalidade da interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) . O método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) Obtém a versão do CSM (Gerenciador de escopo de rastreamento), que informa os clientes se o estado do CSM foi alterado. **ISearchCrawlScopeManager2:: GetVersion** não resulta em uma chamada de processo cruzado. Se a função for bem sucedido, o ponteiro retornado permanecerá válido até que o cliente chame **UnmapViewOfFile** no ponteiro e **CloseHandle** no identificador retornado.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Adicionando raízes ao escopo de rastreamento

O [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) informa ao mecanismo de pesquisa sobre contêineres para rastreamento e/ou inspeção e itens sob esses contêineres para incluir ou excluir. Para adicionar uma nova raiz de pesquisa, crie uma instância de um objeto [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , defina os atributos raiz e, em seguida, chame [**ISearchCrawlScopeManager:: addroot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) e passe-o para um ponteiro para o objeto **ISearchRoot** . A URL da raiz de pesquisa tem a mesma forma que a raiz de pesquisa descrita anteriormente.

A tabela a seguir descreve os métodos Put relevantes para [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); os outros métodos Put da interface não são usados atualmente pelo Windows Search. É recomendável incluir os SIDs (identificadores de segurança) dos usuários em todas as raízes para melhorar a segurança. As raízes por usuário são mais seguras conforme as consultas são executadas em um processo por usuário, garantindo que um usuário não possa ver itens indexados da caixa de entrada de outro usuário, por exemplo.



| Método                     | Descrição                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| colocar \_ ProvidesNotifications | Defina como **true** se um manipulador de protocolo ou outro aplicativo notificará o mecanismo de pesquisa sobre as alterações nas URLs na raiz de pesquisa. A notificação indica que as URLs precisam de reindexação. |
| colocar \_ RootURL               | Define a URL raiz da pesquisa atual. A URL usa o formulário raiz de pesquisa descrito anteriormente.                                                                                                      |



 

 

Por padrão, o indexador não rastreia um escopo quando você adiciona uma raiz de pesquisa. Você também deve adicionar uma regra de inclusão para a raiz. Se você quiser adicionar uma raiz específica do usuário para um aplicativo, esse aplicativo deverá adicionar as raízes apropriadas para novos usuários quando o aplicativo for iniciado.

Para adicionar as raízes apropriadas para novos usuários:

1.  Obtenha o SID do usuário.
2.  Enumere todas as raízes para verificar se existe uma para esse SID.
3.  Adicione uma nova raiz, usando o SID, se necessário.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Removendo raízes do escopo de rastreamento

Você pode usar [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para remover uma raiz do escopo de rastreamento quando não quiser mais que a URL seja indexada. A remoção de uma raiz também exclui todas as regras de escopo dessa URL. Por exemplo, suponha que você deseja desinstalar um repositório de conteúdo e/ou seu manipulador de protocolo de um sistema. Você pode desinstalar o aplicativo, remover todos os dados e, em seguida, remover a raiz de pesquisa do escopo de rastreamento, e o Gerenciador de escopo de rastreamento removerá a raiz e todas as regras de escopo associadas à raiz.

Para remover uma raiz de pesquisa existente, chame [**ISearchCrawlScopeManager:: RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) com a raiz de pesquisa que você deseja remover. A URL da raiz de pesquisa tem a mesma forma que a raiz de pesquisa descrita anteriormente. Esse método retornará S \_ false se a raiz não for encontrada e um código de erro se houvesse um erro ao remover uma raiz que foi encontrada.

A remoção de uma raiz de pesquisa também remove a URL da interface do usuário para as opções de pesquisa do Windows, para que os usuários não possam adicionar novamente esse contêiner ou local usando a interface do usuário. Também é possível remover todas as substituições do conjunto de usuários de uma raiz de pesquisa e reverter para as regras raiz de pesquisa original e escopo. Para obter mais informações, consulte [Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> No Windows Vista, se os usuários forem removidos por meio de perfis de usuário no painel de controle, CSM removerá todas as regras e raízes com seu SID e removerá seus itens indexados do catálogo. No Windows XP, você precisa remover as raízes e as regras dos usuários manualmente.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerando raízes no escopo de rastreamento

O CSM enumera raízes de pesquisa usando uma interface de enumerador de estilo COM padrão, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). Você pode usar essa interface para enumerar raízes de pesquisa para várias finalidades. Por exemplo, talvez você queira exibir todo o escopo de rastreamento em uma interface do usuário ou descobrir se uma raiz específica ou o filho de uma raiz já está no escopo do rastreamento.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



