---
description: Alguns aplicativos armazenam seus itens em bancos de dados ou tipos de arquivo personalizados.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Noções básicas sobre manipuladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760597"
---
# <a name="understanding-protocol-handlers"></a>Noções básicas sobre manipuladores de protocolo

Alguns aplicativos armazenam seus itens em bancos de dados ou tipos de arquivo personalizados. Embora o Windows Search possa indexar o nome e as propriedades do arquivo, o Windows não tem conhecimento do conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no Shell do Windows. Ao criar um manipulador de protocolo, você pode tornar esses itens disponíveis para indexação. Você também pode indexar um formato de arquivo composto, como um arquivo. zip.

Este tópico é organizado da seguinte maneira:

-   [Indexando armazenamentos de dados com manipuladores de protocolo](#indexing-data-stores-with-protocol-handlers)
    -   [Armazenamentos de dados do Shell](#shell-data-stores)
    -   [Manipuladores de protocolo](#protocol-handlers)
    -   [Filtros e manipuladores de protocolo](#filters-and-protocol-handlers)
-   [Indexando um formato de arquivo composto](#indexing-a-compound-file-format)
-   [Tópicos relacionados](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexando armazenamentos de dados com manipuladores de protocolo

Quando os usuários precisam Pesquisar bancos de dados herdados, armazenamentos de email ou outras estruturas que não têm suporte do Windows Search, primeiro você deve determinar se um manipulador de protocolo já existe para esse armazenamento de dados, talvez para uso com outro aplicativo, como o SharePoint Server. Nesse caso, você pode instalar esse manipulador de protocolo no sistema. Os manipuladores de protocolo de pesquisa do Windows usam especificações de design semelhantes ao SharePoint Server e, em geral, podem ser usados de maneira intercambiável.

Para obter mais informações sobre a implantação do Search Server 2008 com o Office SharePoint Server 2007, consulte [servidor de pesquisa de pesquisa federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Armazenamentos de dados do Shell

Antes que um desenvolvedor de terceiros de novos formatos de arquivo e armazenamentos de dados possa obter esses formatos e lojas para que apareçam nos resultados da consulta no Windows Explorer, o desenvolvedor deve implementar uma fonte de dados do Shell. Uma fonte de dados do Shell é um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados. Um repositório de dados é um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação do shell como um contêiner que usa uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo. O manipulador de protocolo implementa o protocolo para acessar uma fonte de conteúdo em seu formato nativo. As interfaces [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) são usadas para implementar um manipulador de protocolo personalizado para expandir as fontes de dados que podem ser indexadas.

Se desejar que os resultados da consulta apareçam no Windows Explorer, você deverá implementar uma fonte de dados do Shell antes de poder criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas forem programáticas (por meio de OLE DB, por exemplo) e interpretadas pelo código do aplicativo em vez do Shell, um namespace de Shell, embora ainda preferido, não é estritamente necessário.

> [!Note]  
> Algumas vezes, uma fonte de dados do Shell é conhecida como extensão de namespace do Shell. Um manipulador é, às vezes, conhecido como uma extensão de shell ou um manipulador de extensão de Shell.

 

Se desejar que os usuários exibam seus resultados de pesquisa no Windows Explorer, você deverá criar um manipulador de protocolo e um ou mais dos seguintes suplementos:

-   Manipulador de menu de atalho
-   Manipulador de ícone
-   Algum outro tipo de manipulador de arquivo

Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "visão geral de manipuladores" no [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md). Para obter informações sobre como criar manipuladores, consulte [registrando extensões de shell](../shell/reg-shell-exts.md), [menu de contexto](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [manipuladores de tipo de arquivo](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Manipuladores de protocolo

Se o repositório de dados também for um contêiner (como uma pasta do sistema de arquivos), você deverá implementar um filtro para enumerar as URLs no contêiner. Se o repositório de dados contiver dados ou tipos de arquivos diferentes de um dos tipos de arquivo 200 com suporte do Windows Search, você deverá implementar um filtro para acessar e indexar o conteúdo dos itens no repositório. O Windows Search usa o manipulador de protocolo e a tecnologia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) semelhante àquela usada pelo SharePoint Server. Se você já tiver filtros para um armazenamento específico e um tipo de arquivo instalado no sistema que está sendo indexado, o Windows Search poderá usar as interfaces existentes para indexar esses dados.

Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md). Para obter informações conceituais sobre manipuladores de filtro, consulte [desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filtros e manipuladores de protocolo

Os manipuladores de protocolo fornecem ao indexador de pesquisa do Windows acesso a armazenamentos de dados, permitindo que o indexador rastreie os nós de um armazenamento de dados e extraia informações relevantes para indexá-los. O Windows Search, por exemplo, é fornecido com manipuladores de protocolo para armazenamentos do sistema de arquivos e para algumas versões de armazenamentos de dados do Microsoft Outlook. Ao indexar email do Outlook, o manipulador de protocolo rastreia todas as mensagens em um conjunto de pastas do Outlook e extrai informações de cada mensagem e anexo. Essas informações são passadas para o indexador para inclusão no catálogo do Windows Search.

Para obter visões gerais do Gerenciador de catálogos e do Gerenciador de escopo de rastreamento (CSM), consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indexando um formato de arquivo composto

Um formato de arquivo composto pode ser indexado para que itens individuais no arquivo possam ser retornados como resultados individuais. Um formato de arquivo composto, como um arquivo compactado com uma extensão de nome de arquivo. zip, é essencialmente um armazenamento de dados e pode ser tratado como tal para fins de indexação. O exemplo a seguir exibe um arquivo. zip no namespace do sistema de arquivos (FILE://c:/test/test.zip) em que há ambas as subpastas e itens individuais.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

O manipulador de protocolo de arquivo descobre quando o FILE://c:/test/test.zip alterações monitorando logs de alteração do sistema de arquivos e invocará um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registrado para arquivos. zip nesse arquivo quando o arquivo for alterado, mas não tiver conhecimento da estrutura interna do próprio arquivo. zip.

Você deve informar ao indexador que o formato de arquivo composto é um armazenamento de dados. É necessário fazer isso para que itens individuais sejam indexados e recuperados como entidades exclusivas. Depois de implementar uma fonte de dados do Shell e executar as etapas a seguir, você terá um manipulador de protocolo que pode processar e expor os dados de um formato de arquivo composto (um arquivo. zip) como itens individuais.

**Para informar ao indexador que um arquivo composto é um armazenamento de dados:**

1.  Crie um manipulador de protocolo (usando [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) ou [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) para arquivos. zip que tem a capacidade de associar ao arquivo de origem. Para obter mais informações, consulte [Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md).

    Por exemplo, você pode usar um caminho de escape para o arquivo. zip como o nome da pasta raiz e, em seguida, usar uma sintaxe de hierarquia como qualquer outro formato de arquivo.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Usando os dados de exemplo acima para c: \\ test \\test.zip, as URLs exclusivas seriam as seguintes. Com essas URLs, o manipulador de protocolo tem as informações necessárias para associar ao arquivo. zip e enumerar as URLs filho, incluindo os arquivos internos, para que eles possam ser vinculados e indexados pelos filtros. doc e. txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Verifique se o manipulador de protocolo atende às duas condições a seguir:
    -   As URLs raiz de um arquivo. zip devem emitir PKEY \_ Search \_ IsClosedDirectory ([System. Search. IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) nas URLs que são as URLs de arquivo. zip raiz. Por exemplo,. zip:///FILE:%2f%2f%2fc:%2ftest% 2ftest.zip/deve emitir IsClosedDirectory = **true**. Isso informa ao indexador que se a data nessa URL não tiver sido alterada, ela não precisa processar nenhuma das URLs filho.
    -   Cada URL filho para essa URL deve emitir PKEY \_ Search \_ IsFullyContained ([System. Search. IsFullyContained](../properties/props-system-search-isfullycontained.md)) nas URLs filho da URL. zip raiz. Normalmente, no final de um rastreamento incremental, o indexador trata todas as URLs não visitadas como itens que devem ser excluídos. Mas o arquivo root. zip não deve processar URLs raiz porque nada foi alterado. A emissão dessa propriedade como **verdadeira** informa ao indexador que, se essa URL não tiver sido processada no final de um rastreamento incremental, ela não deverá ser excluída. Ele só será excluído se o item raiz tiver sido alterado e não for visitado.

O Windows Search requer uma página inicial para um protocolo a fim de saber quais URLs devem ser rastreadas de forma incremental e quais URLs deverão ser ignoradas quando forem encontradas. Mas não podemos começar com uma URL para cada arquivo. zip, porque não sabemos onde cada arquivo. zip é. Portanto, a URL da página inicial do manipulador de protocolo. zip deve ser capaz de enumerar tudo na raiz dos caminhos de escape de todos os arquivos. zip. Esses arquivos. zip não estão necessariamente no namespace FILE: e podem ser uma URL de tipo MAPI que aponta para um arquivo. zip como um anexo, por exemplo.

**Para registrar uma raiz como uma página inicial:**

1.  Registre uma raiz como. zip:///como uma página inicial para que todos os arquivos. zip comecem lá, em vigor. Ao processar o root. zip: URL, seu manipulador de protocolo deve gerar a lista de URLs filho a serem emitidas consultando o Windows Search para todas as URLs com System. FileExtension = ". zip".
2.  Escape essas URLs para remover as barras e retorná-las como URLs filho. Uma consulta de exemplo para recuperar os tipos que você deseja pode ter a seguinte aparência.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Quando o Windows Search faz periodicamente um rastreamento incremental em sua URL raiz. zip:///, você deve refletir de volta a lista de URLs que o Windows Search já está mantendo, que são URLs. zip. Se uma exclusão for descoberta no armazenamento nativo em que o arquivo. zip estiver armazenado, ele não aparecerá na sua enumeração e essa ramificação da árvore no. zip será removida.
4.  Para associar os dados. zip para outro manipulador de protocolo, você deve, idealmente, percorrer o [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) dessa URL para associar ao armazenamento do objeto e não pressupor que seja sempre um arquivo. Isso lhe dá a flexibilidade de trabalhar com anexos em lojas de email, por exemplo.
5.  Ao emitir URLs filho para cada arquivo. zip, você deve usar o PKEY \_ Search \_ UrlToIndexWithModificationTime ([System. Search. UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) para passar PKEY \_ DateModified ([System. DateModified](../properties/props-system-datemodified.md)) do arquivo. zip real para que o indexador rastreie o arquivo. zip somente se ele tiver sido alterado.

Para que suas URLs. zip sejam indexadas imediatamente depois de serem criadas ou modificadas e não precisem esperar que um rastreamento incremental descubra seu novo estado, você pode monitorar o sistema de arquivos por conta própria para alterar o arquivo. zip. No entanto, essa abordagem não funcionaria para outros armazenamentos de dados, como MAPI.

**Para que suas URLs. zip sejam indexadas quando forem criadas ou modificadas:**

1.  Crie um filtro (e a implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para o tipo de arquivo. zip. Para obter mais informações, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](-search-3x-wds-extidx-propertyhandlers.md).
2.  Sempre que a implementação do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é chamada, isso ocorre porque essa URL foi descoberta ou alterada. Em seguida, gere um evento para a URL. zip apropriada para a URL de origem, por meio da interface [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) . Isso lhe dá a capacidade de informar imediatamente ao indexador que há novos dados a serem indexados sem a necessidade de aguardar o rastreamento incremental.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notificando o índice das alterações](-search-3x-wds-notifyingofchanges.md)
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

 

 
