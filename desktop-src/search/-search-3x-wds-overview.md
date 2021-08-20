---
description: Windows A Pesquisa é uma plataforma de pesquisa de área de trabalho que tem funcionalidades de pesquisa instantânea para tipos de arquivo e tipos de dados mais comuns, e desenvolvedores de terceiros podem estender esses recursos para novos tipos de arquivo e tipos de dados.
ms.assetid: 6da601c6-3742-40ad-99f2-8817f7f642b3
title: Visão geral do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a38b757936e9f960d71ac5d1a9759208b4b580af2526e23d4e5d88cde41a206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033124"
---
# <a name="windows-search-overview"></a>Visão geral do Windows Search

Windows A Pesquisa é uma plataforma de pesquisa de área de trabalho que tem funcionalidades de pesquisa instantânea para tipos de arquivo e tipos de dados mais comuns, e desenvolvedores de terceiros podem estender esses recursos para novos tipos de arquivo e tipos de dados.

Este tópico é organizado da seguinte forma:

-   [Introdução](#introduction)
    -   [Serviço Windows Search](#windows-search-service)
    -   [Plataforma de desenvolvimento](#development-platform)
    -   [Interface do Usuário](#user-interface)
-   [Pré-requisitos técnicos](#technical-prerequisites)
    -   [Download e conteúdo do SDK](#sdk-download-and-contents)
-   [Windows Pesquisar documentação do SDK](#windows-search-sdk-documentation)
-   [Histórico de Windows Search](#history-of-windows-search)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Windows A pesquisa é um componente padrão do Windows 7 e Windows Vista e está habilitada por padrão. Windows A pesquisa substitui Windows Pesquisa de Área de Trabalho (WDS), que estava disponível como um complemento para Windows XP e Windows Server 2003.

Windows A pesquisa é composta por três componentes:

-   [Windows serviço de](#windows-search-service) pesquisa (WSS)
-   [Plataforma de desenvolvimento](#development-platform)
-   [Interface do usuário](#user-interface)

### <a name="windows-search-service"></a>Serviço Windows Search

O WSS organiza os recursos extraídos de uma coleção de documentos. O Windows Search Protocol permite que um cliente se comunique com um servidor que está hospedando um WSS, tanto para emitir consultas quanto para permitir que um administrador gerencie o servidor de indexação. Ao processar arquivos, WSS analisa um conjunto de documentos, extrai informações úteis e organiza as informações extraídas para que as propriedades desses documentos possam ser retornadas com eficiência em resposta a consultas.

Uma coleção de documentos que podem ser consultados consiste em um catálogo, que é a unidade de nível mais alto da organização no Windows Search. Um catálogo representa um conjunto de documentos indexados que podem ser consultados. Um catálogo consiste em uma tabela de propriedades com o texto ou o valor e o local correspondente (localidade) armazenados em colunas da tabela. Cada linha da tabela corresponde a um documento separado no escopo do catálogo e cada coluna da tabela corresponde a uma propriedade. Um catálogo pode conter um índice invertido (para correspondência rápida de palavras) e um cache de propriedade (para recuperação rápida de valores de propriedade).

O processo do indexador é implementado como um serviço Windows em execução na conta LocalSystem e está sempre em execução para todos os usuários (mesmo se nenhum usuário estiver conectado), o que permite que o Windows Search realize o seguinte:

-   Mantenha um índice compartilhado entre todos os usuários.
-   Manter restrições de segurança no acesso ao conteúdo.
-   Processe consultas remotas de computadores cliente na rede.

O serviço Pesquisa é projetado para proteger a experiência do usuário e o desempenho do sistema durante a indexação. As seguintes condições faz com que o serviço reduza ou pause a indexação:

-   Alto uso da CPU por processos não relacionados à pesquisa.
-   Alta taxa de E/S do sistema, incluindo leituras e gravações de arquivo, E/S de arquivo de página e cache de arquivos e E/S de arquivo mapeado.
-   Baixa disponibilidade de memória.
-   Pouca vida útil da bateria.
-   Espaço em disco baixo na unidade que armazena o índice.

### <a name="development-platform"></a>Plataforma de desenvolvimento

A maneira preferencial de acessar as APIs de Pesquisa e criar aplicativos Windows Search é por meio de uma fonte de dados do Shell. Uma fonte de dados do Shell é um componente usado para estender o namespace do Shell e expor itens em um armazenamento de dados. Um armazenamento de dados é um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação shell como um contêiner que usa uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema Windows Search usando um manipulador de protocolo.

Por exemplo, [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) é um componente que pode criar instâncias da fonte de dados da pasta de pesquisa, que é uma tipo de fonte de dados "virtual" fornecida pelo Shell que pode executar consultas em outras fontes de dados no namespace do Shell e enumerar resultados. Ele pode fazer isso usando o indexador ou enumerando manualmente e inspecionando itens nos escopos especificados. Essa interface permite configurar os parâmetros da pesquisa usando métodos que criam e modificam pastas de pesquisa. Se os métodos dessa interface não são chamados, os valores padrão são usados em vez disso.

Acessar a funcionalidade Windows Search indiretamente por meio do modelo de dados do Shell é preferencial porque ele fornece acesso à funcionalidade completa do Shell no nível do modelo de dados do Shell. Por exemplo, você pode definir o escopo de uma pesquisa para uma biblioteca (que é um recurso disponível no Windows 7 e posterior) para usar as pastas de biblioteca como o escopo da consulta. Windows A pesquisa agrega os resultados da pesquisa desses locais se eles estão em índices diferentes (se as pastas estão em computadores diferentes). A camada de dados do Shell também cria uma exibição mais completa das propriedades dos itens, sintetizando alguns valores de propriedade. Ele também fornece acesso a recursos de pesquisa para armazenamentos de dados que não são indexados pelo Windows Search. Por exemplo, você pode pesquisar um dispositivo de armazenamento USB (Barramento Serial Universal), um dispositivo portátil que usa o protocolo MTP ou um servidor protocolo FTP (FTP) por meio das fontes de dados do Shell que fornece acesso a esses sistemas de armazenamento. Isso garante uma melhor experiência do usuário.

Windows A pesquisa tem um cache de valores de propriedade que é usado na implementação do Windows Search Service (WSS). Esses valores de propriedade podem ser Windows consultados programaticamente usando o provedor OLE DB Search OLE DB ou por meio de [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa itens nos resultados da pesquisa e exibições baseadas em consulta. Windows A pesquisa coleta e armazena propriedades emitidas por manipuladores de filtro ou manipuladores de propriedades quando um item, como um documento do Word, é indexado. Esse armazenamento é descartado e reconstruído quando o índice é reconstruído.

Os desenvolvedores de terceiros podem criar aplicativos que consomem os dados no índice por meio de consultas programáticas e podem estender os dados no índice para tipos de arquivo e item personalizados a serem indexados pelo Windows Search. Se você quiser mostrar os resultados da consulta Windows Explorer, deverá implementar uma fonte de dados do Shell antes de criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas são programáticas (por OLE DB por exemplo) e interpretadas pelo código do aplicativo em vez do Shell, um namespace do Shell ainda é preferencial, mas não obrigatório.

Um manipulador de protocolo é necessário para Windows obter informações sobre o conteúdo do arquivo, como itens em bancos de dados ou tipos de arquivo personalizados. Embora Windows Search possa indexar o nome e as propriedades do arquivo, Windows não tem informações sobre o conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no shell Windows. Ao implementar um manipulador de protocolo personalizado, você pode expor esses itens. Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "Visão geral dos manipuladores" no [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).

> [!Note]  
> Às vezes, uma fonte de dados do Shell é conhecida como uma extensão de namespace do Shell. Às vezes, um manipulador é conhecido como uma extensão shell ou um manipulador de extensão do Shell.

 

### <a name="user-interface"></a>Interface do Usuário

No Windows Vista e posterior, o Windows Search é integrado a todas as janelas do Windows Explorer para acesso instantâneo à pesquisa. Isso permite que os usuários pesquisem rapidamente arquivos e itens por nome de arquivo, propriedades e conteúdo de texto completo. Os resultados também podem ser filtrados ainda mais para refinar a pesquisa. Aqui estão alguns outros recursos do Windows Search:

-   Uma caixa de pesquisa instantânea em cada janela permite a filtragem instantânea de todos os itens atualmente em exibição. As caixas de pesquisa instantâneas aparecem no menu Iniciar para pesquisar programas ou arquivos e no canto superior direito de todas as janelas Windows Explorer para filtrar os resultados mostrados. A pesquisa instantânea também é integrada a alguns Windows recursos, como Windows Media Player, para encontrar arquivos relacionados.
-   Os documentos podem ser marcados com palavras-chave para a groupá-los por critérios personalizados definidos pelo usuário. As marcas são itens de metadados atribuídos pelo usuário ou aplicativos para facilitar a identificação de arquivos com base em palavras-chave que podem não estar no nome ou conteúdo do item. Por exemplo, um conjunto de imagens pode ser marcado como "Férias do Arizona 2009" para recuperar rapidamente mais tarde pesquisando qualquer uma das palavras incluídas.
-   Os headers de coluna aprimorados Windows exibições do Explorer permitem classificar e agrupar documentos de maneiras diferentes. Por exemplo, os arquivos podem ser classificar de acordo com o nome, a data de modificação, o tipo, o tamanho e as marcas. Os documentos também podem ser agrupados de acordo com qualquer uma dessas propriedades e cada grupo pode ser filtrado (oculto ou exibido) conforme desejado.
-   Os documentos podem ser empilhados de acordo com o nome, a data de modificação, o tipo, o tamanho e as marcas. As pilhas incluem todos os documentos que têm a propriedade especificada e estão localizados em qualquer subpasta da pasta selecionada.
-   As pesquisas podem ser salvas (a serem  recuperadas posteriormente) clicando no botão Salvar Pesquisa no painel de pesquisa no Windows Explorer. Os resultados serão populados dinamicamente com base nos critérios originais quando a pesquisa salva for aberta. Para obter instruções, consulte [Salvar os resultados da pesquisa.](https://windows.microsoft.com/windows-vista/Save-your-search-results)
-   Manipuladores de visualização e manipuladores de miniatura permitem que os usuários visualizem documentos no Windows Explorer sem precisar abrir o aplicativo que os criou.

## <a name="technical-prerequisites"></a>Pré-requisitos técnicos

Antes de começar a ler a Windows do SDK do Search, você deve ter uma compreensão fundamental dos seguintes conceitos:

-   Como implementar uma fonte de dados do Shell.
-   Como implementar um manipulador.
-   Como trabalhar em código nativo.

Uma fonte de dados do Shell é um componente usado para estender o namespace do Shell e expor itens em um armazenamento de dados. No passado, a fonte de dados do Shell era conhecida como extensão de namespace do Shell. Um manipulador é um objeto COM (Component Object Model) que fornece funcionalidade para um item de Shell. para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "visão geral dos manipuladores" na [pesquisa Windows como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).

para obter mais informações sobre o assembly de interoperabilidade do SDK do Windows search para trabalhar com objetos com que são expostos por Windows pesquisa e outros programas que usam código gerenciado, consulte [usando código gerenciado com dados do Shell e Windows pesquisa](-search-3x-wds-managed-code.md). No entanto, observe que os filtros, os manipuladores de propriedade e os manipuladores de protocolo devem ser escritos em código nativo. Isso ocorre devido a possíveis problemas de controle de versão de Common Language Runtime (CLR) com o processo em que vários suplementos são executados. os desenvolvedores que são novos no C++ podem começar a usar o [Visual C++ developer Center](https://msdn.microsoft.com/vstudio//default.aspx) e o [Windows Development Introdução](../desktop-programming.md).

### <a name="sdk-download-and-contents"></a>Download e conteúdo do SDK

além de atender aos prerequisitos técnicos listados, você também deve baixar o [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para obter as bibliotecas de pesquisa de Windows. os [exemplos do SDK de pesquisa Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contêm exemplos de código úteis e um assembly de interoperabilidade para o desenvolvimento com código gerenciado. para obter mais informações sobre como usar os exemplos de código, consulte [Windows exemplos de código de pesquisa](-search-3x-wds-sampleentry.md).

## <a name="windows-search-sdk-documentation"></a>Windows Documentação do SDK de pesquisa

o conteúdo da documentação do SDK do Windows Search é o seguinte:

-   [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md)

    descreve os principais cenários de desenvolvimento na pesquisa Windows. Fornece uma lista de manipuladores identificados pelo cenário de desenvolvimento que você está tentando obter, diretrizes do instalador de suplementos e notas de implementação.

-   [Windows Pesquisar guia do desenvolvedor](-search-developers-guide-entry-page.md)

    Fornece explicações para [gerenciar o índice](-search-3x-wds-mngidx-overview.md), [consultar o índice programaticamente](-search-3x-wds-qryidx-overview.md), [estendendo o índice](-search-3x-wds-extidx-overview.md)e [estendendo recursos de idioma](extending-language-resources-in-windows-search.md).

-   [Windows Referência de pesquisa](-search-reference-entry-page.md)

    documenta as seguintes categorias de Windows interfaces de pesquisa: [manipuladores de protocolo](-search-protocol-handlers-interfaces-entry-page.md), [consulta](-search-querying-interfaces-entry-page.md), [escopo de rastreamento](-search-crawl-scope-interfaces-entry-page.md), suplementos de [dados](-search-data-addins-interfaces-entry-page.md), [gerenciamento de índice](-search-index-mgt-interfaces-entry-page.md)e [notificações](-search-notifications-interfaces-entry-page.md). A documentação de referência também inclui [constantes e enumerações](-search-constants-and-enumerations-entry-page.md), [estruturas](-search-structures-entry-page.md), [mapeamentos de propriedade](-search-3x-wds-propertymappings.md)e o [formato de arquivo de pesquisa salvo](-search-savedsearchfileformat.md).

-   [Windows Exemplos de código de pesquisa](-search-samples-ovw.md)

    Descreve os exemplos de código de API de pesquisa que estão disponíveis.

-   [Pesquisa federada no Windows](-search-federated-search-overview.md)

    descreve o suporte a Windows 7 para a federação de pesquisa para armazenamentos de dados remotos usando OpenSearch tecnologias que permitem que os usuários acessem e interajam com seus dados remotos no Windows Explorer.

-   [Tecnologias de pesquisa relacionadas](-search-3x-wds-sampleentry.md)

    lista as tecnologias relacionadas ao Windows search: pesquisa de Enterprise, SharePoint Enterprise search e aplicativos herdados, como o Windows Desktop Search 2. x e Platform SDK: serviço de indexação.

-   [Windows Pesquisar Glossário](search-glossary.md)

    define termos essenciais usados em tecnologias de Windows de pesquisa e Shell.

## <a name="history-of-windows-search"></a>histórico de pesquisa de Windows

Windows a pesquisa substitui Windows o WDS (Desktop search), que estava disponível como um suplemento para Windows XP e Windows Server 2003. o WDS substituiu o serviço de indexação herdado de versões anteriores do Windows com aprimoramentos de desempenho, usabilidade e extensibilidade. A nova plataforma de desenvolvimento dá suporte a requisitos que produzem um sistema mais seguro e estável. embora a nova plataforma de consulta não seja compatível com o Microsoft Windows Desktop Search (WDS) 2. x, os filtros e manipuladores de protocolo escritos para versões anteriores do WDS podem ser atualizados para trabalhar com Windows pesquisa. Windows A pesquisa também dá suporte a um novo sistema de propriedades. Para obter informações sobre filtros, manipuladores de propriedades e manipuladores de protocolo, consulte [estendendo o índice](-search-3x-wds-extidx-overview.md).

Windows a pesquisa é incorporada ao Windows Vista e posterior e está disponível como uma atualização redistribuível para o WDS 2. x, para dar suporte aos seguintes sistemas operacionais:

-   versões de 32 bits do Windows XP com Service Pack 2 (SP2).
-   todas as versões baseadas em x64 do Windows XP.
-   Windows Server 2003 com Service Pack 1 (SP1) e posterior.
-   todas as versões baseadas em x64 do Windows Server 2003.

os sistemas que executam esses sistemas operacionais devem ter o Windows search instalado para executar aplicativos escritos para Windows pesquisa. para obter mais informações, consulte [o artigo 917013 da base de dados de conhecimento: descrição de Windows desktop search 3, 1 e o Interface de Usuário Multilíngue Pack para Windows Desktop search 3, 1](https://support.microsoft.com/kb/917013).

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions//bb776815(v=vs.85)).
-   Para obter mais informações sobre o [ISearchFolderItemFactory](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) e a fonte de dados da pasta DB, consulte a descrição da constante de análise de Str \_ \_ com \_ Propriedades em [chaves de cadeia de caracteres de contexto de associação](../shell/str-constants.md). Consulte também [matrizes de associação](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [IPropertySystem:: GetPropertyDescriptionListFromString](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Para obter informações sobre OLE DB, consulte [visão geral da programação de OLE DB](/cpp/data/oledb/ole-db-programming-overview?view=vs-2019). para obter informações sobre o Provedor de Dados de .NET Framework para OLE DB, consulte a documentação do [Namespace System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1&preserve-view=true) .
-   para obter uma visão geral dos manipuladores de tipo de arquivo (também conhecidos como manipuladores de extensão de Shell e manipuladores de pesquisa), consulte [Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md).
-   para ver as placas de mensagens com suporte da comunidade sobre as tecnologias de pesquisa, consulte [fórum do MSDN: desenvolvimento Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   para obter exemplos de código relacionados, consulte [Windows exemplos de código de pesquisa](-search-samples-ovw.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Search como uma plataforma de desenvolvimento](-search-3x-wds-development-ovr.md)
</dt> <dt>

[idiomas com suporte da pesquisa Windows](-search-3x-wds-language-support.md)
</dt> <dt>

[Usar código gerenciado com os dados do Shell e do Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
