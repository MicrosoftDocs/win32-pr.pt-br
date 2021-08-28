---
description: O Gerenciador do Escopo de Rastreamento (CSM) permite adicionar e remover raízes de pesquisa para seus armazenamentos de dados de e para o escopo de rastreamento Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gerenciando raízes de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbe5fe6184681e6c37cb0b6a7f9a35c677fec53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880194"
---
# <a name="managing-search-roots"></a>Gerenciando raízes de pesquisa

O Gerenciador do Escopo de Rastreamento (CSM) permite adicionar e remover raízes de pesquisa para seus armazenamentos de dados de e para o escopo de rastreamento Windows Search.

Este tópico abrange os seguintes assuntos:

-   [Sobre raízes de pesquisa](#about-search-roots)
-   [Antes de começar](#before-you-begin)
-   [Windows 7: Nova API de Gerenciador do Escopo de Rastreamento](#windows-7-new-crawl-scope-manager-api)
-   [Adicionando raízes ao escopo de rastreamento](#adding-roots-to-the-crawl-scope)
-   [Removendo raízes do escopo de rastreamento](#removing-roots-from-the-crawl-scope)
-   [Enumerando raízes no escopo de rastreamento](#enumerating-roots-in-the-crawl-scope)
-   [Tópicos relacionados](#related-topics)

 

## <a name="about-search-roots"></a>Sobre raízes de pesquisa

Uma raiz de pesquisa define a base de um namespace do Shell em que escopos específicos podem ser incluídos ou excluídos e geralmente é o contêiner de nível mais alto em um protocolo que pode ser enumerado. Ele não especifica quais partes desse armazenamento devem ou não ser indexadas; ele simplesmente sinaliza que um armazenamento de conteúdo existe e está associado a um manipulador de protocolo registrado. A sintaxe para identificar uma URL raiz de pesquisa inclui o protocolo, o identificador de segurança do armazenamento ou do usuário, o caminho e, opcionalmente, um item específico (como um arquivo). Os exemplos a seguir mostram duas formas da sintaxe para uma raiz de pesquisa.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



O segmento de protocolo deve ser seguido por duas &lt; (2) barras ('/'), a menos que seja o arquivo: protocolo, que requer três barras &gt; (file:///). O segmento representa um armazenamento de conteúdo ou um identificador de segurança do usuário se a raiz da pesquisa <site or SID> deve ser específica para o usuário. O segmento de caminho é um conjunto de contêineres, como diretórios ou pastas, e pode incluir o &lt; &gt; caractere curinga ' \* '. O &lt; segmento de item é opcional e também pode incluir o caractere &gt; curinga ' \* '. Se você não incluir um item, certifique-se de concluir o segmento de caminho com uma barra ou o indexador assumirá que o último subcontidor é um item.

Por exemplo, suponha que você implementou um manipulador de protocolo (myPH) para manipular arquivos do tipo \* .myext para um aplicativo personalizado. Todos esses arquivos estarão localizados na pasta WorkteamA \\ ProjectFiles em um computador local. A raiz da pesquisa para que pode ter esta aparência:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Suponha que você planeja incluir todos os arquivos .myext, mas nada mais desse contêiner no índice. A raiz da pesquisa para que pode ter esta aparência:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* .myext.

Padrões curinga definem URLs usando o caractere curinga ' ' e são considerados um padrão em vez de uma URL, mas a terminologia geralmente é \* usada de forma intercambiável. Por exemplo, file:///C: \\ os dados do ProjectA \\ \* \\ \\ corresponderiam às seguintes URLs:

-   C: \\ Dados do ProjectA \\ **versão1** \\\\
-   C: \\ Dados do ProjectA \\ **versão2** \\\\

Mas esse padrão não corresponderia a esta URL:

-   C: \\ Dados temporários \\ **da versão1 \\ do** \\ ProjectA\\

Você deve criar novas raízes de pesquisa para contêineres que ainda não estão no escopo de rastreamento do indexador. Se o caminho C: ParentScope já estiver incluído no escopo de rastreamento, você não precisará adicionar uma nova raiz de pesquisa para \\ C: ParentScope ChildScope, a menos que você saiba que o escopo filho foi excluído \\ \\ anteriormente.

A interface do usuário para definir Windows Search exibe raízes de pesquisa para os usuários para que eles possam refinar as regras de escopo para suas pesquisas. Como parte do processo de instalação para seu manipulador de protocolo personalizado, contêiner e/ou aplicativo, você pode definir um escopo de rastreamento padrão, com regras de inclusão e exclusão. Essas regras são apresentadas aos usuários finais como locais. Os usuários podem navegar dentro dos subdiretivos de sua raiz de pesquisa predefinida e selecionar aqueles que eles querem incluir em pesquisas ou limpar aqueles que deseja excluir.

 

## <a name="before-you-begin"></a>Antes de começar

Antes de usar qualquer uma das interfaces Gerenciador do Escopo de Rastreamento (CSM), você deve executar as seguintes etapas de pré-requisito:

1.  Crie o **objeto CrawlSearchManager** e obtenha sua interface [**ISearchManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)
2.  Chame [**ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) para "SystemIndex" para obter uma instância de uma interface [**ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)
3.  Chame [**ISearchCatalogManager::GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) para obter uma instância da interface [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

Depois de fazer alterações no Gerenciador do Escopo de Rastreamento (CSM), você deve chamar [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Esse método não aceita parâmetros e retorna S \_ OK em caso de êxito.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: Nova API de Gerenciador do Escopo de Rastreamento

No **Windows 7 e** posterior, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende a funcionalidade da interface [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) O [**método ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) obtém a versão Gerenciador do Escopo de Rastreamento (CSM), que informa aos clientes se o estado do CSM foi alterado. **ISearchCrawlScopeManager2::GetVersion** não resulta em uma chamada entre processos. Se a função for bem-sucedida, o ponteiro retornado permanecerá válido até que o cliente chama **UnmapViewOfFile** no ponteiro e **CloseHandle** no alça retornado.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Adicionando raízes ao escopo de rastreamento

O [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) informa ao mecanismo de pesquisa sobre contêineres para rastrear e/ou observar e itens nesses contêineres para incluir ou excluir. Para adicionar uma nova raiz de pesquisa, insinue um objeto [**ISearchRoot,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) de definir os atributos raiz e, em seguida, chame [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) e passe um ponteiro para o objeto **ISearchRoot.** A URL raiz da pesquisa tem o mesmo formato que a raiz de pesquisa descrita anteriormente.

A tabela a seguir descreve os métodos put relevantes para [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); Os outros métodos put da interface não são usados atualmente pelo Windows Search. É recomendável incluir os SIDs (identificadores de segurança) dos usuários em todas as raízes para maior segurança. As raízes por usuário são mais seguras à medida que as consultas são executados em um processo por usuário, garantindo que um usuário não possa ver itens indexados na caixa de entrada de outro usuário, por exemplo.



| Método                     | Descrição                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Defina **como TRUE** se um manipulador de protocolo ou outro aplicativo notificar o mecanismo de pesquisa sobre alterações nas URLs na raiz da pesquisa. A notificação indica que as URLs precisam de reindexação. |
| put \_ RootURL               | Define a URL raiz da pesquisa atual. A URL assume o formulário raiz de pesquisa descrito anteriormente.                                                                                                      |



 

 

Por padrão, o indexador não rastrea um escopo quando você adiciona uma raiz de pesquisa. Você também deve adicionar uma regra de inclusão para a raiz. Se você quiser adicionar uma raiz específica do usuário para um aplicativo, esse aplicativo deverá adicionar as raízes apropriadas para novos usuários quando o aplicativo for iniciado.

Para adicionar as raízes apropriadas para novos usuários:

1.  Obter o SID do usuário.
2.  Enumere todas as raízes para verificar se existe uma para esse SID.
3.  Adicione uma nova raiz, usando o SID, se necessário.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Removendo raízes do escopo de rastreamento

Você pode usar [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para remover uma raiz do escopo de rastreamento quando não quiser mais que essa URL seja indexada. A remoção de uma raiz também exclui todas as regras de escopo para essa URL. Por exemplo, suponha que você queira desinstalar um armazenamento de conteúdo e/ou seu manipulador de protocolo de um sistema. Você pode desinstalar o aplicativo, remover todos os dados e, em seguida, remover a raiz da pesquisa do escopo de rastreamento, e o Gerenciador do Escopo de Rastreamento removerá a raiz e todas as regras de escopo associadas à raiz.

Para remover uma raiz de pesquisa existente, chame [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) com a raiz de pesquisa que você deseja remover. A URL raiz da pesquisa tem o mesmo formato que a raiz de pesquisa descrita anteriormente. Esse método retornará S FALSE se a raiz não for encontrada e um código de erro se houver um erro ao remover \_ uma raiz encontrada.

A remoção de uma raiz de pesquisa também remove a URL da interface do usuário para as opções Windows Search, portanto, os usuários podem não ser capazes de adicionar esse contêiner ou local usando a interface do usuário. Também é possível remover todas as substituições definidas pelo usuário de uma raiz de pesquisa e reverter para as regras de escopo e raiz de pesquisa originais. Para obter mais informações, consulte [Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> No Windows Vista, se os usuários são removidos por meio de Perfis de Usuário no Painel de Controle, o CSM remove todas as regras e raízes com seu SID e remove seus itens indexados do catálogo. No Windows XP, você precisa remover manualmente as raízes e as regras dos usuários.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerando raízes no escopo de rastreamento

O CSM enumera raízes de pesquisa usando uma interface de enumerador de estilo COM padrão, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). Você pode usar essa interface para enumerar raízes de pesquisa para várias finalidades. Por exemplo, talvez você queira exibir todo o escopo de rastreamento em uma interface do usuário ou descobrir se uma raiz específica ou o filho de uma raiz já está no escopo de rastreamento.

 

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

**Conceitual**
</dt> <dt>

[Usando o Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Gerenciando regras de escopo](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



