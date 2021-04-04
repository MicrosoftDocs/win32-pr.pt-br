---
description: Para indexar o conteúdo e as propriedades dos novos formatos de arquivo e armazenamentos de dados, o Microsoft Windows Search deve ser estendido com suplementos.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search como uma plataforma de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646885"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search como uma plataforma de desenvolvimento

Para indexar o conteúdo e as propriedades dos novos formatos de arquivo e armazenamentos de dados, o Microsoft Windows Search deve ser estendido com suplementos.

Antes que um desenvolvedor de terceiros de novos formatos de arquivo e armazenamentos de dados possa obter esses formatos e lojas para que apareçam nos resultados da consulta no Windows Explorer, o desenvolvedor deve fazer as três coisas a seguir:

-   Implemente uma fonte de dados do Shell para estender o namespace do Shell.
-   Expor itens em um repositório de dados (se eles estiverem adicionando um novo armazenamento de dados, porque ele precisaria ser indexado).
-   Desenvolva um manipulador de protocolo para que o Windows Search possa acessar os dados para indexação.

Este tópico é organizado da seguinte maneira:

-   [Introdução](#getting-started)
-   [Visão geral dos cenários de desenvolvimento de pesquisa](#overview-of-search-development-scenarios)
    -   [Adicionando um novo armazenamento de dados](#adding-a-new-data-store)
    -   [Adicionando um novo formato de arquivo](#adding-a-new-file-format)
    -   [Consumindo resultados da pesquisa do Windows](#consuming-windows-search-results)
-   [Visão geral dos manipuladores](#overview-of-handlers)
-   [Diretrizes do instalador do suplemento](#add-in-installer-guidelines)
-   [Observação para implementadores](#note-to-implementers)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="getting-started"></a>Introdução

Antes de começar a criar um aplicativo de pesquisa do Windows, lembre-se de que a maneira preferida de fazer isso é por meio de uma fonte de dados do Shell. Uma fonte de dados do Shell estende o namespace do Shell e expõe os itens em um armazenamento de dados. Os itens no armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo. Essa abordagem indireta para acessar o Windows Search implementando uma fonte de dados do Shell é preferida porque fornece acesso à funcionalidade completa do Shell. Fazer isso dessa forma garante uma experiência de usuário razoável.

Se desejar que os resultados da consulta apareçam no Windows Explorer, você deverá implementar uma fonte de dados do Shell antes de poder criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas forem programáticas (por meio de OLE DB, por exemplo) e interpretadas pelo código do aplicativo em vez do Shell, um namespace de shell ainda será preferível, mas não obrigatório.

Um manipulador de protocolo é necessário para que o Windows obtenha conhecimento do conteúdo do arquivo, como itens em bancos de dados ou tipos de arquivo personalizados. Embora o Windows Search possa indexar o nome e as propriedades do arquivo, o Windows não tem conhecimento do conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no Shell do Windows. Ao implementar um manipulador de protocolo personalizado, você pode expor esses itens. Para obter uma lista de manipuladores identificados pelo cenário do desenvolvedor que você está tentando obter, consulte [visão geral dos manipuladores](#overview-of-handlers).

## <a name="overview-of-search-development-scenarios"></a>Visão geral dos cenários de desenvolvimento de pesquisa

Os cenários de desenvolvimento mais comuns no Windows Search são:

-   [Adicionando um novo armazenamento de dados](#adding-a-new-data-store)
-   [Adicionando um novo formato de arquivo](#adding-a-new-file-format)
-   [Consumindo resultados da pesquisa do Windows](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Adicionando um novo armazenamento de dados

Você precisará de um armazenamento de dados do Shell para Windows Search somente se estiver adicionando um novo armazenamento de dados a ser indexado. Um repositório de dados é um repositório de dados que podem ser expostos ao modelo de programação do shell como um contêiner usando uma fonte de dados do Shell. Os itens em um armazenamento de dados podem então ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo. O manipulador de protocolo implementa o protocolo para acessar uma fonte de conteúdo em seu formato nativo. As interfaces [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) são usadas para implementar um manipulador de protocolo personalizado para expandir as fontes de dados que podem ser indexadas. Para obter informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Adicionando um novo formato de arquivo

Se você adicionar um novo formato de arquivo personalizado, será necessário desenvolver um manipulador de filtro ou um manipulador de propriedades, mas não ambos. Um filtro é uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Ele abre arquivos de um tipo de arquivo específico e filtra as propriedades e partes do texto do indexador. Os filtros são associados a tipos de arquivo, como indicado pelas extensões de nome de arquivo, tipos de MIME ou identificadores de classe (CLSIDs). Embora um filtro possa lidar com vários tipos de arquivo, cada tipo de arquivo funciona com apenas um filtro.

Um manipulador de propriedades traduz os dados armazenados em um arquivo em um esquema estruturado que é reconhecido pelo e pode ser acessado pelo Windows Explorer, pelo Windows Search e por outros aplicativos. Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para um arquivo. Os dados traduzidos incluem exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante. Cada manipulador de propriedade é associado a um tipo de arquivo específico, identificado pela extensão de nome de arquivo. Você precisa de um manipulador de propriedades para fazer o seguinte:

-   Mostrar propriedades de item não indexadas na interface do usuário.
-   Suporte à gravação de propriedades.

### <a name="consuming-windows-search-results"></a>Consumindo resultados da pesquisa do Windows

As seções a seguir descrevem várias maneiras de consumir os resultados da pesquisa do Windows:

-   [Consultando dados](#querying-data)
-   [Consultando armazenamentos de dados remotos (pesquisa federada)](#querying-remote-data-stores-federated-search)
-   [Indexando arquivos e itens](#indexing-files-and-items)
-   [Indexando um armazenamento de dados](#indexing-a-data-store)
-   [Gerenciando o processo de indexação](#managing-the-indexing-process)
-   [Integrando o sistema de propriedades do Windows com aplicativos Windows Search](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Consultar Dados

Os desenvolvedores que escrevem aplicativos sobre o Windows Search combinado e o sistema de propriedades do Windows podem acessar arquivos e itens, independentemente do aplicativo ou tipo de arquivo. Há duas maneiras de os aplicativos acessarem os dados do indexador:

-   Os aplicativos se comunicam diretamente com o OLE DB enviando consultas do Windows Search linguagem SQL (SQL) para o provedor de OLE DB do Windows Search para recuperar os resultados. As consultas podem ser construídas manualmente ou usando a interface [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para gerar o SQL a partir de palavras-chave de pesquisa e AQS (sintaxe de consulta avançada).
-   Os aplicativos funcionam por meio da camada do Shell. A vantagem da camada de Shell é que ela também oferece suporte a outras fontes como o grep. No entanto, a desvantagem é que nem todos os recursos do indexador estão disponíveis.

Outra opção é usar os protocolos Search-MS://e search://, que executam pesquisas baseadas em URL renderizadas por meio do Windows Explorer. Essa opção habilita o desenvolvimento de peso mais leve, mas não retorna resultados ou seleções de usuário da exibição de resultados para o aplicativo de chamada. Além disso, como outros protocolos, os aplicativos de pesquisa de terceiros podem assumir os protocolos de pesquisa-MS://e search://se os aplicativos estiverem em conformidade com o conjunto de recursos necessário. Para obter mais informações sobre a consulta, consulte [consultar o processo no Windows Search](querying-process--windows-search-.md) e [consultar o índice programaticamente](-search-3x-wds-qryidx-overview.md).

### <a name="querying-remote-data-stores-federated-search"></a>Consultando armazenamentos de dados remotos (pesquisa federada)

No Windows 7 e posterior, a pesquisa federada oferece um novo provedor de pesquisa que consulta armazenamentos de dados remotos por meio de servidores Web, por meio do protocolo [OpenSearch](https://github.com/dewitt/opensearch) , e enumera os resultados como RSS ou Atom feeds XML. Os conectores de pesquisa são junções de namespace que simulam o comportamento da pasta usando um provedor de pesquisa. Para obter mais informações sobre a Federação de pesquisa para armazenamentos de dados remotos no Windows 7, consulte [pesquisa federada no Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indexando arquivos e itens

O conteúdo que é indexado baseia-se nos tipos de arquivo e dados com suporte por meio de suplementos incluídos no Windows Search e das regras de inclusão e exclusão padrão para pastas no sistema de arquivos. Por exemplo, os filtros incluídos na pesquisa de janela dão suporte a mais de 200 tipos comuns de dados, incluindo Microsoft Office documentos, email do Microsoft Outlook (em conjunto com o manipulador de protocolo MAPI), arquivos de texto sem formatação, HTML e muito mais. Para obter uma lista completa de tipos de arquivo com suporte nativo, consulte [o que está incluído no índice](-search-3x-wds-included-in-index.md).

O índice pode ser estendido com manipuladores de propriedade e filtros para expor o conteúdo e as propriedades dos novos formatos de arquivo para o índice e o Windows Explorer. Filtros são uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Há dois tipos de filtros: um que interage com itens individuais, como arquivos, e um que interage com contêineres como pastas. Os filtros são de várias finalidades, pois dão suporte a dados de agrupamento, conteúdo de texto, algumas propriedades e vários idiomas.

Por outro lado, os manipuladores de propriedade têm uma finalidade mais específica: para expor as propriedades de tipos de arquivo específicos que são identificadas pelas extensões de nome de arquivo. Um manipulador de propriedades para um tipo de arquivo pode habilitar as propriedades Get e set e pode enumerar as propriedades associadas a esse tipo de arquivo. Ao contrário dos filtros, os manipuladores de propriedades não dão suporte a dados de texto ou de conteúdo de textos, e os manipuladores de propriedade não têm como indicar em qual idioma uma propriedade de texto está, a menos que ofereçam suporte a propriedades de gravação.

### <a name="indexing-a-data-store"></a>Indexando um armazenamento de dados

O índice pode ser estendido com manipuladores de protocolo para fornecer acesso a armazenamentos de dados proprietários. Por exemplo, arquivos e itens contidos em armazenamentos de dados do sistema de arquivos que não são de arquivo (como bancos de dados e armazenamentos de email) exigem um manipulador de protocolo para mapear de uma URL para um fluxo. Os manipuladores de protocolo também podem determinar opcionalmente os filtros corretos a serem usados para extrair informações de um fluxo. Os filtros enumeram as URLs do repositório de dados. Os itens são então indexados individualmente usando o filtro apropriado e/ou o manipulador de propriedade. Para obter mais informações, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Gerenciando o processo de indexação

Os desenvolvedores de aplicativos podem controlar o escopo e a frequência da indexação do Windows Search usando várias interfaces de gerenciamento. Essas interfaces incluem a funcionalidade para adicionar e remover os diretórios que o indexador verifica em busca de alterações, notificar manualmente o índice das alterações nos dados, verificar o status do indexador e forçar a reindexação de alguns ou de todos os dados. Para obter mais informações, consulte [Gerenciando o índice](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>Integrando o sistema de propriedades do Windows com aplicativos Windows Search

O sistema de propriedades do Windows é um sistema de leitura/gravação extensível de definições de dados que fornece uma maneira uniforme de expressar os metadados sobre itens de Shell. O sistema de propriedades do Windows no Windows Vista e posterior permite que você armazene e recupere metadados para itens de Shell. Um item de Shell é qualquer conteúdo único, como um arquivo, uma pasta, um email ou um contato. Uma propriedade é uma parte individual dos metadados associados a um item de Shell. Os valores de propriedade são expressos como uma estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Uma lista extensa de propriedades comuns está incluída para vários tipos de itens comuns, como fotos, música, documentos, mensagens, contatos e arquivos. Os desenvolvedores também podem introduzir suas próprias propriedades para a plataforma se nenhuma propriedade existente atender às suas necessidades. Para obter mais informações sobre como integrar aplicativos com o sistema de propriedades do Windows, consulte [desenvolvendo manipuladores de propriedade](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Visão geral dos manipuladores

Um manipulador é um objeto COM (Component Object Model) que fornece funcionalidade para um item de Shell. A maioria das fontes de dados de shell oferece um sistema extensível para ligar manipuladores a itens. Por exemplo, a pasta sistema de arquivos usa o sistema de associação para pesquisar os manipuladores de um determinado tipo de arquivo. Um manipulador específico é necessário para cada tipo de arquivo. Um manipulador de filtro é necessário para o tipo de arquivo Adobe Acrobat. pdf, por exemplo, outro manipulador de filtro é necessário para o formato de arquivo. doc e assim por diante.

Manipuladores diferentes têm alguma semelhança. No Windows Vista e posterior, todos os manipuladores devem usar uma das seguintes interfaces para inicializar o manipulador: [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

A tabela a seguir lista as tarefas de desenvolvimento de alto nível, o tipo de manipulador necessário para cada tarefa e fornece um link para informações conceituais sobre como executar cada tarefa.



| Tarefa                                                                                                                                                            | Manipulador                          | Informações conceituais                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acessando as propriedades de um arquivo para indexação                                                                                                                 | Manipulador de propriedades                 | [Desenvolvendo manipuladores de propriedade](-search-3x-wds-extidx-propertyhandlers.md)<br/> [Propriedades definidas pelo sistema para formatos de arquivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Adicionar formatos de área de transferência para o objeto de dados ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) de um item (objetos de dados são usados em cenários de arrastar e soltar e copiar/colar.) | Manipulador de objeto de dados              | [Criando manipuladores de dados](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Adicionando verbos para um item que são normalmente exibidos em um menu de atalho                                                                                         | Manipulador de menu de atalho            | [Criando manipuladores de menu de contexto](../shell/context-menu-handlers.md)<br/> [Personalizando um menu de atalho usando verbos dinâmicos](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Associando um tipo de arquivo a um ícone específico                                                                                                                    | Manipulador de ícone                     | [Criando manipuladores de ícones](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Criando folhas de propriedades com imagens e controles da interface do usuário que permitem a interação personalizada com um tipo de arquivo                                                          | Manipulador de folha de propriedades           | [Manipuladores de folha de propriedades](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Habilitando um tipo de item para dar suporte a cenários de arrastar e soltar e copiar/colar                                                                                         | Descartar manipulador                     | [Transferindo objetos do shell com o recurso de arrastar e soltar e a área de transferência](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Extraindo partes de propriedades de texto e de documento para indexação                                                                                                  | Manipulador de filtro                   | [Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indexando um novo tipo de arquivo                                                                                                                                        | Manipulador de filtro, manipulador de propriedades | [Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)<br/> [Desenvolvendo manipuladores de propriedade](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indexando o conteúdo de um armazenamento de dados                                                                                                                           | Manipulador de protocolo                 | [Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)                                                                                                                                            |
| Visualizando uma exibição simplificada do item de Shell no painel de visualização do Windows Explorer                                                                             | Gerenciador de visualização                  | [Gerenciadores de visualização](../shell/preview-handlers.md)                                                                                                                                                             |
| Fornecendo texto pop-up quando um mouse passa sobre um objeto de interface do usuário                                                                                                      | Manipulador de infodicas                  | [Criando manipuladores de extensão de shell](../shell/handlers.md) (personalização de infotip)                                                                                                                            |
| Fornecendo uma imagem estática para representar um item de Shell                                                                                                              | Manipulador de miniaturas                | [Manipuladores de miniatura](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

A tabela a seguir lista os manipuladores e as interfaces para implementar cada tipo de manipulador.



| Manipulador                | Interfaces                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descartar manipulador           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), [**IDropTargetHelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Manipulador de objeto de dados    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Manipulador de filtro         | [**Visio**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Manipulador de ícone           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Opcional: [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| Manipulador de infodicas        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Gerenciador de visualização        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Manipulador de propriedades       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Manipulador de protocolo       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol), [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Opcional: [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2), [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2), [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3), [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Manipulador de folha de propriedades | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Manipulador de menu de atalho  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Manipulador de miniaturas      | [**Manipuladordeminiaturai**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> Um manipulador de propriedades, às vezes, é kown como um manipulador de metadados. Algumas vezes, uma fonte de dados do Shell é conhecida como extensão de namespace do Shell. Um manipulador de tipo de arquivo é, às vezes, conhecido como um manipulador de extensão de shell ou uma extensão de Shell.

 

Para obter mais informações sobre como criar manipuladores, consulte [criando manipuladores de extensão de shell](../shell/handlers.md). Para obter mais informações sobre propriedades, consulte [sistema de propriedades do Windows](../properties/windows-properties-system.md).

## <a name="add-in-installer-guidelines"></a>Diretrizes do instalador do suplemento

Use as seguintes diretrizes ao criar um instalador de suplemento:

-   O instalador deve usar o instalador EXE ou MSI.
-   As notas de versão devem ser fornecidas.
-   Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.
-   O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.
-   Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um suplemento mais recente tiver substituído um suplemento anterior, o usuário deverá ser capaz de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão novamente para esse tipo de arquivo ou repositório.

## <a name="note-to-implementers"></a>Observação para implementadores

Antes de criar um filtro ou manipulador de propriedades, os desenvolvedores devem considerar o seguinte:

-   Esses manipuladores são extensões em processo que são carregadas em processos que você não controla, como o processo de daemon de filtro, o Windows Explorer (pesquisa com grep) e hosts de terceiros como o Windows Mail.
-   Você deve escrever um código seguro que seja robusto o suficiente para manipular formulários corrompidos arbitrariamente do formato de arquivo que foram criados para atacar o sistema.
-   Seu suplemento não deve vazar recursos que produzirão problemas para os processos de host.
-   Seu suplemento não deve falhar, pois isso também causará uma falha nos processos de host e tornará o processo de filtragem lento.
-   Como esses manipuladores são executados em um processo do sistema em segundo plano, eles devem executar rapidamente com um mínimo de CPU e e/s consumidos para atender aos requisitos de desempenho do sistema.

Portanto, esses suplementos devem ser escritos por desenvolvedores com experiência na criação de código de nível de sistema.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   Para fontes de dados que precisam usar o objeto de exibição de pasta do sistema padrão do Shell (DefView), consulte [implementando uma exibição de pasta](../lwef/nse-folderview.md), função [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) e [**SFV \_ criar**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) estrutura. As fontes de dados que usam o objeto de exibição de pasta do sistema padrão do Shell (DefView) devem implementar o seguinte conjunto de interfaces: [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)e (opcionalmente) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Se a implementação do **IShellFolder** não usar o **SHCreateShellFolderView** para criar o DefView, o objeto de exibição do Shell poderá precisar de [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview).
-   [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) é a interface primária para os consumidores da fonte de dados do Shell conhecida como DBFolder. Para obter mais informações sobre DBFolder, consulte a descrição da constante de análise de STR \_ \_ com \_ Propriedades em [**chaves de cadeia de caracteres de contexto de associação**](../shell/str-constants.md). Consulte também [matrizes de associação](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [**IPropertySystem:: GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte a documentação do [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .
-   Para placas de mensagens com suporte da Comunidade em tecnologias de pesquisa, consulte [Windows: fóruns de pesquisa](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) no msdn.
-   Para obter exemplos de código relacionados, consulte [exemplos de código do Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Idiomas com suporte do Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Usar código gerenciado com os dados do Shell e do Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Guia do desenvolvedor do Windows Search](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 
