---
description: O Windows Search é uma plataforma de pesquisa de desktop que tem recursos de pesquisa instantânea para os tipos de arquivos e dados mais comuns, e desenvolvedores de terceiros podem estender esses recursos para novos tipos de dados e tipo de arquivo.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Visão geral do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee4cde62ce663c47ab4cafac0c74ca220fe6faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826921"
---
# <a name="windows-search-overview"></a>Visão geral do Windows Search

O Windows Search é uma plataforma de pesquisa de desktop que tem recursos de pesquisa instantânea para os tipos de arquivos e dados mais comuns, e desenvolvedores de terceiros podem estender esses recursos para novos tipos de dados e tipo de arquivo.

Este tópico é organizado da seguinte maneira:

-   [Introdução](#introduction)
    -   [Serviço Windows Search](#windows-search-service)
    -   [Plataforma de desenvolvimento](#development-platform)
    -   [Interface do usuário](#user-interface)
-   [Pré-requisitos técnicos](#technical-prerequisites)
    -   [Download e conteúdo do SDK](#sdk-download-and-contents)
-   [Documentação do SDK do Windows Search](#windows-search-sdk-documentation)
-   [Histórico da pesquisa do Windows](#history-of-windows-search)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O Windows Search é um componente padrão do Windows 7 e do Windows Vista e é habilitado por padrão. O Windows Search substitui o WDS (Windows Desktop Search), que estava disponível como um suplemento para o Windows XP e o Windows Server 2003.

O Windows Search é composto por três componentes:

-   [Windows serviço de pesquisa](#windows-search-service) (WSS)
-   [Plataforma de desenvolvimento](#development-platform)
-   [Interface do usuário](#user-interface)

### <a name="windows-search-service"></a>Serviço Windows Search

O WSS organiza os recursos extraídos de uma coleção de documentos. O protocolo de pesquisa do Windows permite que um cliente se comunique com um servidor que hospeda um WSS, tanto para emitir consultas quanto para permitir que um administrador gerencie o servidor de indexação. Ao processar arquivos, o WSS analisa um conjunto de documentos, extrai informações úteis e, em seguida, organiza as informações extraídas para que as propriedades desses documentos possam ser retornadas de forma eficiente em resposta a consultas.

Uma coleção de documentos que podem ser consultados abrange um catálogo, que é a unidade de nível mais alta da organização no Windows Search. Um catálogo representa um conjunto de documentos indexados que podem ser consultados. Um catálogo consiste em uma tabela de propriedades com o texto ou o valor e o local correspondente (localidade) armazenados em colunas da tabela. Cada linha da tabela corresponde a um documento separado no escopo do catálogo, e cada coluna da tabela corresponde a uma propriedade. Um catálogo pode conter um índice invertido (para correspondência rápida de palavras) e um cache de Propriedades (para recuperação rápida de valores de propriedade).

O processo do indexador é implementado como um serviço do Windows em execução na conta LocalSystem e está sempre em execução para todos os usuários (mesmo que nenhum usuário esteja conectado), o que permite que o Windows Search realize o seguinte:

-   Mantenha um índice compartilhado entre todos os usuários.
-   Manter restrições de segurança no acesso ao conteúdo.
-   Processar consultas remotas de computadores cliente na rede.

O serviço de pesquisa foi projetado para proteger a experiência do usuário e o desempenho do sistema durante a indexação. As seguintes condições fazem com que o serviço seja limitado ou Pause a indexação:

-   Alto uso da CPU por processos não relacionados à pesquisa.
-   Alta taxa de e/s do sistema, incluindo leituras e gravações de arquivos, arquivo de paginação e e/s do cache de arquivos e e/s de arquivo mapeado.
-   Disponibilidade de memória insuficiente.
-   Vida útil de bateria baixa.
-   Pouco espaço em disco na unidade que armazena o índice.

### <a name="development-platform"></a>Plataforma de desenvolvimento

A maneira preferida de acessar as APIs de pesquisa e criar aplicativos de pesquisa do Windows é por meio de uma fonte de dados do Shell. Uma fonte de dados do Shell é um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados. Um repositório de dados é um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação do shell como um contêiner que usa uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.

Por exemplo, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) é um componente que pode criar instâncias da fonte de dados da pasta de pesquisa, que é um tipo de fonte de dados "virtual" fornecida pelo shell que pode executar consultas em outras fontes de dados no namespace do Shell e enumerar resultados. Isso pode ser feito usando o indexador ou enumerando manualmente e inspecionando itens nos escopos especificados. Essa interface permite que você configure os parâmetros da pesquisa usando métodos que criam e modificam pastas de pesquisa. Se os métodos dessa interface não forem chamados, os valores padrão serão usados em seu lugar.

O acesso ao recurso de pesquisa do Windows indiretamente por meio do modelo de dados do Shell é preferencial porque fornece acesso à funcionalidade completa do Shell no nível do modelo de dados do Shell. Por exemplo, você pode definir o escopo de uma pesquisa para uma biblioteca (que é um recurso disponível no Windows 7 e posterior) para usar as pastas de biblioteca como o escopo da consulta. Em seguida, o Windows Search agrega os resultados da pesquisa desses locais se eles estiverem em índices diferentes (se as pastas estiverem em computadores diferentes). A camada de dados do Shell também cria uma exibição mais completa das propriedades dos itens, sintetizando alguns valores de propriedade. Ele também fornece acesso aos recursos de pesquisa para armazenamentos de dados que não são indexados pelo Windows Search. Por exemplo, você pode pesquisar dispositivos de armazenamento USB (barramento serial universal), dispositivos portáteis que usam o protocolo MTP ou um servidor de protocolo FTP (FTP) por meio das fontes de dados do shell que fornecem acesso a esses sistemas de armazenamento. Isso garante uma melhor experiência do usuário.

O Windows Search tem um cache de valores de propriedade que é usado na implementação do Windows Serviço de Pesquisa (WSS). Esses valores de propriedade podem ser consultados programaticamente usando o provedor de OLE DB do Windows Search ou por meio de [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa os itens nos resultados da pesquisa e exibições baseadas em consulta. Em seguida, o Windows Search coleta e armazena as propriedades emitidas por manipuladores de filtro ou manipuladores de propriedades quando um item, como um documento do Word, é indexado. Esse armazenamento é Descartado e recriado quando o índice é recriado.

Desenvolvedores de terceiros podem criar aplicativos que consomem os dados no índice por meio de consultas programáticas e podem estender os dados no índice para tipos de arquivo e item personalizados a serem indexados pelo Windows Search. Se você quiser mostrar os resultados da consulta no Windows Explorer, deverá implementar uma fonte de dados do Shell antes de poder criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas forem programáticas (por meio de OLE DB, por exemplo) e interpretadas pelo código do aplicativo em vez do Shell, um namespace de shell ainda será preferível, mas não obrigatório.

Um manipulador de protocolo é necessário para que o Windows Obtenha informações sobre o conteúdo do arquivo, como itens em bancos de dados ou tipos de arquivo personalizados. Embora o Windows Search possa indexar o nome e as propriedades do arquivo, o Windows não tem informações sobre o conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no Shell do Windows. Ao implementar um manipulador de protocolo personalizado, você pode expor esses itens. Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "visão geral de manipuladores" no [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).

> [!Note]  
> Algumas vezes, uma fonte de dados do Shell é conhecida como extensão de namespace do Shell. Um manipulador é, às vezes, conhecido como uma extensão de shell ou um manipulador de extensão de Shell.

 

### <a name="user-interface"></a>Interface do Usuário

No Windows Vista e posterior, o Windows Search é integrado a todas as janelas do Windows Explorer para acesso instantâneo à pesquisa. Isso permite que os usuários pesquisem arquivos e itens rapidamente por nome de arquivo, propriedades e conteúdo de texto completo. Os resultados também podem ser filtrados para refinar a pesquisa. Aqui estão alguns outros recursos do Windows Search:

-   Uma caixa de pesquisa instantânea em cada janela permite a filtragem instantânea de todos os itens atualmente na exibição. As caixas de pesquisa instantânea aparecem no menu Iniciar para procurar programas ou arquivos e no canto superior direito de todas as janelas do Windows Explorer para filtrar os resultados mostrados. A pesquisa instantânea também é integrada a alguns outros recursos do Windows, como o Windows Media Player, para encontrar arquivos relacionados.
-   Os documentos podem ser marcados com palavras-chave para agrupá-los por critérios personalizados que são definidos pelo usuário. Marcas são itens de metadados que são atribuídos pelo usuário ou aplicativos para facilitar a localização de arquivos com base em palavras-chave que podem não estar no nome ou no conteúdo do item. Por exemplo, um conjunto de imagens pode ser marcado como "férias do Arizona 2009" para recuperar-se rapidamente mais tarde, pesquisando por qualquer uma das palavras incluídas.
-   Os cabeçalhos de coluna aprimorados nas exibições do Windows Explorer permitem classificar e agrupar documentos de maneiras diferentes. Por exemplo, os arquivos podem ser classificados de acordo com o nome, data de modificação, tipo, tamanho e marcas. Os documentos também podem ser agrupados de acordo com qualquer uma dessas propriedades e cada grupo pode ser filtrado (oculto ou exibido) conforme desejado.
-   Os documentos podem ser empilhados de acordo com o nome, data de modificação, tipo, tamanho e marcas. As pilhas incluem todos os documentos que têm a propriedade especificada e estão localizados em qualquer subpasta da pasta selecionada.
-   As pesquisas podem ser salvas (para serem recuperadas mais tarde) clicando no botão **Salvar pesquisa** no painel Pesquisar do Windows Explorer. Os resultados serão repopulados dinamicamente com base nos critérios originais quando a pesquisa salva for aberta. Para obter instruções, consulte [salvar os resultados da pesquisa](https://windows.microsoft.com/windows-vista/Save-your-search-results).
-   Os gerenciadores de visualização e os manipuladores de miniatura permitem que os usuários visualizem documentos no Windows Explorer sem precisar abrir o aplicativo que os criou.

## <a name="technical-prerequisites"></a>Pré-requisitos técnicos

Antes de começar a ler a documentação do SDK do Windows Search, você deve ter uma compreensão fundamental dos seguintes conceitos:

-   Como implementar uma fonte de dados do Shell.
-   Como implementar um manipulador.
-   Como trabalhar em código nativo.

Uma fonte de dados do Shell é um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados. No passado, a fonte de dados do Shell era chamada de extensão de namespace do Shell. Um manipulador é um objeto COM (Component Object Model) que fornece funcionalidade para um item de Shell. Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "visão geral de manipuladores" no [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).

Para obter mais informações sobre o assembly de interoperabilidade do SDK do Windows Search para trabalhar com objetos COM que são expostos pelo Windows Search e outros programas que usam código gerenciado, consulte [usando código gerenciado com dados do Shell e pesquisa do Windows](-search-3x-wds-managed-code.md). No entanto, observe que os filtros, os manipuladores de propriedade e os manipuladores de protocolo devem ser escritos em código nativo. Isso ocorre devido a possíveis problemas de controle de versão de Common Language Runtime (CLR) com o processo em que vários suplementos são executados. Os desenvolvedores que são novos no C++ podem começar a usar o [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx) e o [desenvolvimento do Windows introdução](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Download e conteúdo do SDK

Além de atender aos Prerequisitos técnicos listados, você também deve baixar o [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para obter as bibliotecas de pesquisa do Windows. Os [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contêm exemplos de código úteis e um assembly de interoperabilidade para o desenvolvimento com código gerenciado. Para obter mais informações sobre como usar os exemplos de código, consulte [exemplos de código do Windows Search](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Documentação do SDK do Windows Search

O conteúdo da documentação do SDK do Windows Search é o seguinte:

-   [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md)

    Descreve os principais cenários de desenvolvimento no Windows Search. Fornece uma lista de manipuladores identificados pelo cenário de desenvolvimento que você está tentando obter, diretrizes do instalador de suplementos e notas de implementação.

-   [Guia do desenvolvedor do Windows Search](-search-developers-guide-entry-page.md)

    Fornece explicações para [gerenciar o índice](-search-3x-wds-mngidx-overview.md), [consultar o índice programaticamente](-search-3x-wds-qryidx-overview.md), [estendendo o índice](-search-3x-wds-extidx-overview.md)e [estendendo recursos de idioma](extending-language-resources-in-windows-search.md).

-   [Referência do Windows Search](-search-reference-entry-page.md)

    Documenta as seguintes categorias de interfaces de pesquisa do Windows: [manipuladores de protocolo](-search-protocol-handlers-interfaces-entry-page.md), [consulta](-search-querying-interfaces-entry-page.md), [escopo de rastreamento](-search-crawl-scope-interfaces-entry-page.md), suplementos de [dados](-search-data-addins-interfaces-entry-page.md), [Gerenciamento de índice](-search-index-mgt-interfaces-entry-page.md)e [notificações](-search-notifications-interfaces-entry-page.md). A documentação de referência também inclui [constantes e enumerações](-search-constants-and-enumerations-entry-page.md), [estruturas](-search-structures-entry-page.md), [mapeamentos de propriedade](-search-3x-wds-propertymappings.md)e o [formato de arquivo de pesquisa salvo](-search-savedsearchfileformat.md).

-   [Exemplos de código do Windows Search](-search-samples-ovw.md)

    Descreve os exemplos de código de API de pesquisa que estão disponíveis.

-   [Pesquisa federada no Windows](-search-federated-search-overview.md)

    Descreve o suporte do Windows 7 para a Federação de pesquisa para armazenamentos de dados remotos usando tecnologias OpenSearch que permitem que os usuários acessem e interajam com seus dados remotos no Windows Explorer.

-   [Tecnologias de pesquisa relacionadas](-search-3x-wds-sampleentry.md)

    Lista as tecnologias relacionadas ao Windows Search: Enterprise Search, SharePoint Enterprise Search e aplicativos herdados, como o Windows Desktop Search 2. x e Platform SDK: serviço de indexação.

-   [Glossário do Windows Search](search-glossary.md)

    Define termos essenciais usados nas tecnologias de shell e de pesquisa do Windows.

## <a name="history-of-windows-search"></a>Histórico da pesquisa do Windows

O Windows Search substitui o WDS (Windows Desktop Search), que estava disponível como um suplemento para o Windows XP e o Windows Server 2003. O WDS substituiu o serviço de indexação herdado de versões anteriores do Windows por aprimoramentos de desempenho, usabilidade e extensibilidade. A nova plataforma de desenvolvimento dá suporte a requisitos que produzem um sistema mais seguro e estável. Embora a nova plataforma de consulta não seja compatível com o Microsoft Windows Desktop Search (WDS) 2. x, os filtros e manipuladores de protocolo escritos para versões anteriores do WDS podem ser atualizados para funcionar com o Windows Search. O Windows Search também dá suporte a um novo sistema de propriedades. Para obter informações sobre filtros, manipuladores de propriedades e manipuladores de protocolo, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).

O Windows Search é integrado ao Windows Vista e posterior e está disponível como uma atualização redistribuível para o WDS 2. x, para dar suporte aos seguintes sistemas operacionais:

-   versões de 32 bits do Windows XP com Service Pack 2 (SP2).
-   Todas as versões baseadas em x64 do Windows XP.
-   Windows Server 2003 com Service Pack 1 (SP1) e posterior.
-   Todas as versões baseadas em x64 do Windows Server 2003.

Os sistemas que executam esses sistemas operacionais devem ter o Windows Search instalado para executar aplicativos escritos para o Windows Search. Para obter mais informações, consulte [o artigo 917013 da base de dados de conhecimento: Descrição do Windows desktop search 3, 1 e o Multilingual User Interface Pack para Windows desktop search 3, 1](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions//bb776815(v=vs.85)).
-   Para obter mais informações sobre o [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) e a fonte de dados da pasta DB, consulte a descrição da constante de análise de Str \_ \_ com \_ Propriedades em [chaves de cadeia de caracteres de contexto de associação](../shell/str-constants.md). Consulte também [matrizes de associação](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [IPropertySystem:: GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019). Para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte a documentação do [namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   Para obter uma visão geral dos manipuladores de tipo de arquivo (também conhecidos como manipuladores de extensão de shell e manipuladores de pesquisa), consulte [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).
-   Para ver as placas de mensagens com suporte da Comunidade sobre tecnologias de pesquisa, consulte [Fórum do MSDN: desenvolvimento do Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   Para obter exemplos de código relacionados, consulte [exemplos de código do Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Idiomas com suporte do Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Usar código gerenciado com os dados do Shell e do Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
