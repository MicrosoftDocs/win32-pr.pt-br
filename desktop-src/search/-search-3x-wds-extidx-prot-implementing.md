---
description: Alguns aplicativos armazenam seus itens em bancos de dados ou tipos de arquivo personalizados.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Noções básicas sobre manipuladores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f466d2d329fda81eee4533dc4444250abc42e0a4e8187d603a290acb277e3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119352246"
---
# <a name="understanding-protocol-handlers"></a>Noções básicas sobre manipuladores de protocolo

Alguns aplicativos armazenam seus itens em bancos de dados ou tipos de arquivo personalizados. Embora Windows Search possa indexar o nome e as propriedades do arquivo, Windows não tem conhecimento do conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no shell Windows. Ao criar um manipulador de protocolo, você pode disponibilizar esses itens para indexação. Você também pode indexar um formato de arquivo composto, como um .zip arquivo.

Este tópico é organizado da seguinte forma:

-   [Indexando armazenamentos de dados com manipuladores de protocolo](#indexing-data-stores-with-protocol-handlers)
    -   [Armazenamentos de dados do Shell](#shell-data-stores)
    -   [Manipuladores de protocolo](#protocol-handlers)
    -   [Filtros e manipuladores de protocolo](#filters-and-protocol-handlers)
-   [Indexando um formato de arquivo composto](#indexing-a-compound-file-format)
-   [Tópicos relacionados](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexando armazenamentos de dados com manipuladores de protocolo

Quando os usuários precisam pesquisar bancos de dados herdados, armazenamentos de email ou outras estruturas de dados que não têm suporte no Windows Search, você deve primeiro determinar se um manipulador de protocolo já existe para esse armazenamento de dados, talvez para uso com outro aplicativo, como o SharePoint Server. Nesse caso, você pode instalar esse manipulador de protocolo no sistema. Windows Os manipuladores de protocolo de pesquisa usam especificações de design semelhantes SharePoint Server e geralmente podem ser usados de forma intercambiável.

Para obter mais informações sobre a implantação do Search Server 2008 com o Office SharePoint Server 2007, consulte [Federated \[ Search Server \] 2008](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Armazenamentos de dados do Shell

Antes que um desenvolvedor de terceiros de novos formatos de arquivo e armazenamentos de dados possa fazer com que esses formatos e armazenamentos apareçam nos resultados da consulta no Windows Explorer, o desenvolvedor deve implementar uma fonte de dados do Shell. Uma fonte de dados do Shell é um componente usado para estender o namespace do Shell e expor itens em um armazenamento de dados. Um armazenamento de dados é um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação shell como um contêiner que usa uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema Windows Search usando um manipulador de protocolo. O manipulador de protocolo implementa o protocolo para acessar uma fonte de conteúdo em seu formato nativo. As interfaces [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) são usadas para implementar um manipulador de protocolo personalizado para expandir as fontes de dados que podem ser indexadas.

Se você quiser que os resultados da consulta apareçam Windows Explorer, implemente uma fonte de dados do Shell antes de criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas serão programáticas (por meio de OLE DB por exemplo) e interpretadas pelo código do aplicativo em vez do Shell, um namespace do Shell, embora ainda preferencial, não será estritamente necessário.

> [!Note]  
> Às vezes, uma fonte de dados do Shell é conhecida como uma extensão de namespace do Shell. Às vezes, um manipulador é conhecido como uma extensão do Shell ou um manipulador de extensão do Shell.

 

Se você quiser que os usuários vejam os resultados da pesquisa no Windows Explorer, você deverá criar um manipulador de protocolo e um ou mais dos seguintes complementos:

-   Manipulador de menu de atalho
-   Manipulador de ícones
-   Algum outro tipo de manipulador de arquivos

Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "Visão geral dos manipuladores" no [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md). Para obter informações sobre como criar manipuladores, consulte [Registrando extensões de shell,](../shell/reg-shell-exts.md) [menu de](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))contexto e [manipuladores de tipo de arquivo](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Manipuladores de protocolo

Se o armazenamento de dados também for um contêiner (como uma pasta do sistema de arquivos), você deverá implementar um filtro para enumerar as URLs no contêiner. Se o armazenamento de dados contiver dados ou tipos de arquivo diferentes de um dos 200 tipos de arquivo com suporte do Windows Search, você deverá implementar um filtro para acessar e indexar o conteúdo dos itens no armazenamento. Windows A pesquisa usa o manipulador de protocolo e a [**tecnologia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) semelhante à usada pelo SharePoint Server. Se você já tiver filtros para um tipo de arquivo e armazenamento específicos instalados no sistema que está sendo indexado, o Windows Search poderá usar as interfaces existentes para indexar esses dados.

Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md). Para obter informações conceituais sobre manipuladores de filtro, consulte [Desenvolvendo manipuladores de filtro.](-search-ifilter-conceptual.md)

### <a name="filters-and-protocol-handlers"></a>Filtros e manipuladores de protocolo

Os manipuladores de protocolo dão ao indexador Windows Search acesso aos armazenamentos de dados, permitindo que o indexador rastrea os nós de um armazenamento de dados e extraia informações relevantes para o índice. Windows Pesquise, por exemplo, é fornecidas com manipuladores de protocolo para armazenamentos de sistema de arquivos e para algumas versões de armazenamentos de dados Outlook Microsoft. Ao indexar Outlook email, o manipulador de protocolo rastrea todas as mensagens em um conjunto de Outlook pastas e extrai informações de cada mensagem e anexo. Essas informações são passadas para o indexador para inclusão no catálogo Windows Search.

Para ter visão geral do Gerenciador de Catálogo e Gerenciador do Escopo de Rastreamento (CSM), consulte [Usando](-search-3x-wds-mngidx-catalog-manager.md) o Gerenciador de Catálogo e [Usando o Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indexando um formato de arquivo composto

Um formato de arquivo composto pode ser indexado para que itens individuais no arquivo possam ser retornados como resultados individuais. Um formato de arquivo composto, como um arquivo compactado com uma extensão .zip nome de arquivo, é essencialmente um armazenamento de dados e pode ser tratado como tal para fins de indexação. O exemplo a seguir exibe um .zip no namespace do sistema de arquivos (FILE://c:/test/test.zip) no qual há subpastas e itens individuais.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

O manipulador de protocolo FILE descobre quando o FILE://c:/test/test.zip muda monitorando logs de alteração do sistema de arquivos e invoca um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registrado para arquivos .zip nesse arquivo quando o arquivo é alterado, mas não tem conhecimento da estrutura interna do próprio arquivo .zip.

Você deve informar ao indexador que o formato de arquivo composto é um armazenamento de dados. É necessário fazer isso para que itens individuais sejam indexados e recuperados como entidades exclusivas. Depois de implementar uma fonte de dados do Shell e realizar as etapas a seguir, você terá um manipulador de protocolo que pode processar e expor os dados de um formato de arquivo composto (um arquivo .zip) como itens individuais.

**Para informar o indexador de que um arquivo composto é um armazenamento de dados:**

1.  Crie um manipulador de protocolo (usando [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) ou [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) para arquivos .zip que têm a capacidade de se vincular ao arquivo de origem. Para obter mais informações, [consulte Instalando e registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md).

    Por exemplo, você pode usar um caminho de escape para o arquivo .zip como o nome da pasta raiz e, em seguida, usar uma sintaxe de hierarquia como qualquer outro formato de arquivo.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Usando os dados de exemplo acima para c: testetest.zip, as \\ \\ URLs exclusivas seriam as a seguir. Com essas URLs, o manipulador de protocolo tem as informações necessárias para se vincular ao arquivo .zip e enumerar as URLs filho, incluindo os arquivos internos, para que possam ser vinculadas e indexadas pelos filtros .doc e .txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Verifique se o manipulador de protocolo atende às duas condições a seguir:
    -   As URLs raiz de um arquivo .zip devem emitir IsClosedDirectory de Pesquisa PKEY \_ \_ ([System.Search.IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) nas URLs que são as URLs de arquivo .zip raiz. Por exemplo, .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ deve emitir IsClosedDirectory = **TRUE**. Isso informa ao indexador que, se a data nessa URL não tiver sido alterada, ele não precisará processar nenhuma das URLs filho.
    -   Cada URL filho para essa URL deve emitir a Pesquisa de PKEY \_ \_ IsFullyContained ([System.Search.IsFullyContained](../properties/props-system-search-isfullycontained.md)) nas URLs filho da URL .zip raiz. Normalmente, no final de um rastreamento incremental, o indexador trata todas as URLs não pesquisadas como itens que devem ser excluídos. Mas o arquivo .zip raiz não deve processar URLs raiz porque nada foi alterado. A emissão dessa propriedade como **TRUE** informa ao indexador que, se essa URL não tiver sido processada no final de um rastreamento incremental, ela não deverá ser excluída. Ele só será excluído se o item raiz tiver sido alterado e não for visitado.

Windows A pesquisa requer uma página inicial para um protocolo para saber quais URLs rastrear incrementalmente e quais URLs devem ser ignoradas quando elas são encontradas. Mas não podemos começar com uma URL para cada arquivo .zip, porque não sabemos onde cada arquivo .zip está. Portanto, .zip URL da página inicial do manipulador de protocolo deve ser capaz de enumerar tudo na raiz dos caminhos de escape de todos os .zip arquivos. Esses .zip arquivos não estão necessariamente no namespace FILE: e podem ser uma URL de tipo MAPI que aponta para um arquivo .zip como um anexo, por exemplo.

**Para registrar uma raiz como uma página inicial:**

1.  Registre uma raiz como .zip:/// como uma página inicial para que todos os .zip de dados comecem lá, na verdade. Ao processar a URL do .zip: raiz, o manipulador de protocolo deve gerar a lista de URLs filho a emitir consultando Windows Search para todas as URLs com System.FileExtension = ".zip".
2.  Escape dessas URLs para remover as barras e devolvê-las como URLs filho. Uma consulta de exemplo para recuperar os tipos que você deseja pode ser a seguinte.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Quando Windows Search periodicamente faz um rastreamento incremental em sua URL raiz .zip:///, você deve refletir a lista de URLs que o Windows Search já está mantendo que .zip URLs. Se uma exclusão for descoberta no armazenamento nativo em que o arquivo .zip está armazenado, ele não aparecerá na enumeração e esse branch da árvore no .zip será removido.
4.  Para se vincular aos dados .zip para outro manipulador de protocolo, o ideal é passar pelo [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para que essa URL seja vinculada ao armazenamento do objeto e não pressupor que seja sempre um arquivo. Isso proporciona a flexibilidade de trabalhar com anexos em lojas de email, por exemplo.
5.  Ao emitir URLs filho para cada arquivo .zip, você deve usar Url de Pesquisa \_ PKEYToIndexWithModificationTime \_ ([System.Search.UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) para passar PKEY \_ DateModified ([System.DateModified](../properties/props-system-datemodified.md)) do arquivo .zip real para que o indexador rastrea o arquivo .zip somente se ele tiver sido alterado.

Para que as URLs do .zip sejam indexadas imediatamente depois que elas são criadas ou modificadas e não precisam esperar um rastreamento incremental descobrir seu novo estado, você pode monitorar o sistema de arquivos por conta própria para .zip de arquivos. No entanto, essa abordagem não funcionaria para outros armazenamentos de dados, como MAPI.

**Para que suas urLs .zip sejam indexadas quando elas são criadas ou modificadas:**

1.  Crie um filtro (e implementação da interface [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) para o tipo .zip arquivo. Para obter mais informações, consulte [Desenvolvendo manipuladores de propriedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md).
2.  Sempre que [**sua implementação de IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é chamada, é porque essa URL foi descoberta ou alterada. Em seguida, gere um evento para .zip URL apropriada para a URL de origem, por meio da interface [**IGatherNotifyInline.**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) Isso oferece a capacidade de dizer imediatamente ao indexador que há novos dados a serem indexados sem precisar aguardar o rastreamento incremental.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Instalando e registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notificando o índice de alterações](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Adicionando ícones e menus de contexto](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemplo de código: extensões de shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalando e registrando manipuladores de protocolo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Criando um conector de pesquisa para um manipulador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Manipuladores de protocolo de depuração](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
