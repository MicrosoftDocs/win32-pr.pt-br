---
title: Windows Desktop Search 2. x
description: Entenda o Windows Desktop Search 2. x. Para versões do Windows posteriores ao Windows XP e ao Windows Server 2003, use o Windows Search em vez disso.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ff43f827458d295e54b71b3f39c7aa471c058d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408119"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

O uso do e do desenvolvimento para as versões 2. x do Microsoft Windows Desktop Search (WDS) é fortemente desencorajado em favor do [Windows Search](../search/-search-3x-wds-overview.md).

O WDS é um serviço de indexação e uma plataforma que fornece pesquisa rápida de arquivos e dados em diferentes fontes de dados e locais. O WDS ajuda os usuários e outros aplicativos a encontrar quase tudo em seus computadores, mensagens de email, compromissos de calendário, fotos, documentos e muito mais. Além disso, o WDS pode retornar resultados de várias fontes de dados em um ambiente do Windows Explorer para que os usuários possam visualizar, filtrar e agir rapidamente nos resultados da pesquisa.

O WDS indexa dados dentro de um determinado escopo de rastreamento, os locais especificados em um computador local e uma rede compartilhada que o indexador deve rastrear. Esse escopo de rastreamento pode ser controlado por opções definidas pelo usuário, APIs de gerenciamento e políticas de grupo, que os administradores de rede podem configurar para controlar as permissões de acesso do usuário e as configurações de indexação. As políticas de grupo podem restringir o acesso a determinados recursos de rede, bem como definir os recursos a serem indexados.

Esta seção contém os seguintes tópicos:

-   [Visão geral](#windows-desktop-search-2x)
    -   [Sobre o indexador do WDS](#about-the-wds-indexer)
    -   [Sobre o catálogo do WDS](#about-the-wds-catalog)
    -   [Sobre o mecanismo de pesquisa e os resultados](#about-the-search-engine-and-results)
-   [Desenvolvendo com o WDS](#developing-with-wds)
    -   [Adicionando dados ao índice com suplementos](#adding-data-to-the-index-with-add-ins)
    -   [Consultando o índice](#querying-the-index)
-   [Requisitos de compatibilidade](#compatibility-requirements)
    -   [Requisitos do sistema](#system-requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

### <a name="about-the-wds-indexer"></a>Sobre o indexador do WDS

Quando instalado pela primeira vez, o indexador rastreia os arquivos mais comuns voltados para o usuário na pasta meus documentos, nas pastas de email do Microsoft Outlook e do Microsoft Outlook Express e nos locais especificados no Política de Grupo. Os usuários também podem especificar novos arquivos e locais para que o indexador inclua (ou exclua) em rastreamentos sucessivos. Cada local incluído é identificado por URL, e o indexador será iniciado nessa URL e iterará recursivamente em todas as subpastas ou locais até que todos os itens tenham sido indexados. Um escopo é um conjunto de URLs. As APIs de gerenciamento podem ser usadas por aplicativos personalizados para definir seu escopo de rastreamento, um conjunto de URLs que apontam para caminhos dentro de um protocolo, como `file://` para pastas em uma unidade ou `mapi:// ` para armazenamentos de email MAPI, como o Outlook. O WDS usa manipuladores de protocolo para acessar os armazenamentos de dados e filtros para analisar e indexar o texto e as propriedades dos itens. Esses dados são armazenados no catálogo.

### <a name="about-the-wds-catalog"></a>Sobre o catálogo do WDS

O catálogo do WDS é um índice de texto e propriedades coletados de itens em email especificado, unidades locais, recursos de rede e outros armazenamentos de dados locais. O conteúdo do catálogo se baseia em opções e regras definidas pelo WDS, aplicativos criados na plataforma do WDS, preferências do usuário e políticas de grupo. Há mais de 200 propriedades disponíveis para cada item indexado, como data de criação, tamanho e propriedades específicas de tipo ("de" para mensagens de email). Para obter uma lista dessas propriedades, consulte a [referência de esquema](-search-2x-wds-schematable.md)do WDS.

### <a name="about-the-search-engine-and-results"></a>Sobre o mecanismo de pesquisa e os resultados

Na Deskbar do WDS ou no Windows Explorer, os usuários podem pesquisar o conteúdo de texto completo e os metadados de propriedade de itens indexados. Os mesmos tipos de pesquisas também podem ser iniciados na linha de comando, em uma página da Web ou em um aplicativo personalizado. O mecanismo de pesquisa do WDS localiza itens que correspondem aos critérios de pesquisa e os retorna como conjuntos de resultados do Microsoft ActiveX Data Objects (ADO). O WDS exibe itens que correspondem aos critérios de pesquisa e pode apresentar uma visualização avançada do item. Você pode criar aplicativos para interceptar a consulta de pesquisa, executar a pesquisa e/ou exibir o conjunto de resultados.

## <a name="developing-with-wds"></a>Desenvolvendo com o WDS

Há dois tipos principais de integração com o WDS: adicionar dados ao índice e consultar o conteúdo do índice para recuperar registros que correspondem aos critérios de pesquisa.

### <a name="adding-data-to-the-index-with-add-ins"></a>Adicionando dados ao índice com Add-Ins

Há basicamente dois tipos de fontes de dados: armazenamentos do sistema de arquivos e armazenamentos de sistema que não são arquivos. Um grupo de arquivos em meus documentos é um armazenamento de sistema de arquivos simples. O WDS pode pesquisar informações nos arquivos armazenados nesse sistema de arquivos, caso ele possa localizar um filtro para o tipo de arquivo. Você pode habilitar o WDS para indexar um novo tipo de arquivo proprietário se fornecer uma implementação da interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para esse tipo de arquivo.

Um armazenamento de sistema que não seja de arquivo, como um banco de dados, requer um manipulador de protocolo para permitir que o WDS Navegue e indexe dados no repositório de dados. Por exemplo, se você tiver um cliente de email que armazena sua lista de emails recebidos em seu próprio arquivo (como arquivos PST no Outlook), você pode fornecer um manipulador de protocolo para indexar e pesquisar cada email individual fornecendo um manipulador de protocolo. Se o armazenamento de dados for hierárquico, você também precisará implementar uma interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para enumerar os itens no repositório. Para uma melhor experiência de usuário, você pode implementar uma extensão de Shell para fornecer menus de contexto e ícones de dentro da exibição de resultados.

Atualmente, o WDS contém filtros para mais de 200 tipos de itens (incluindo itens de texto sem formatação, como HTML, XML e arquivos de código-fonte) e usa a mesma tecnologia de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e manipulador de protocolo que os serviços do SharePoint. Se você já tiver filtros instalados para tipos de arquivo proprietários, o WDS poderá usar as interfaces de filtro existentes para indexar esses dados.

### <a name="querying-the-index"></a>Consultando o índice

O WDS fornece aplicativos com conjuntos de resultados personalizados de dados do índice com base em qualquer um dos valores de esquema disponíveis. Os resultados são retornados como conjuntos de registros ADO. Há quatro maneiras de incorporar as consultas do WDS em um aplicativo, cada uma oferecendo vários níveis de personalização e robustez.

-   Interface ISearchDesktop – as APIs nessa interface são usadas para chamar o WDS de forma programática, especificando uma cadeia de caracteres de consulta, uma lista de colunas a serem retornadas, restrições de escopo semelhantes a uma cláusula WHERE de linguagem SQL (SQL) e o nome da coluna pela qual classificar. Essas APIs estão disponíveis para código nativo e gerenciado.
-   Controle ActiveX do WDS – esse controle desenha a interface de pesquisa do WDS e gerencia a pesquisa e a exibição de resultados. Esse método é mais fácil do que usar as APIs, mas é menos flexível. Para usar esse controle em um aplicativo Microsoft Visual Studio, vá para a caixa de diálogo **escolher itens da caixa de ferramentas** no menu **ferramentas** e adicione "Visualizador de resultados do Windows Desktop Search" à **caixa de ferramentas** da guia **componentes com** . Em seguida, adicione o controle ao formulário no qual você deseja incluí-lo. O controle ActiveX do WDS é compatível com o WDS 2. x e 3. x somente no Windows XP.
-   Parâmetros de linha de comando – os aplicativos podem chamar o executável do WDS com vários parâmetros para pesquisar e exibir resultados. Isso abrirá uma janela do WDS com os resultados exibidos. Essa é a maneira mais fácil de adicionar a pesquisa a um aplicativo, mas não retorna ao aplicativo de chamada todas as informações sobre o que o usuário faz dentro da janela do WDS.
-   Objeto auxiliar de navegador do WDS (BHO) – da mesma forma, as páginas da Web podem usar o BHO para enviar consultas ao WDS ou ao aplicativo de pesquisa registrado. Depois de validar a URL de páginas da Web em relação à lista de segurança de domínio do WDS, o WDS executará a consulta e exibirá os resultados usando a interface de pesquisa padrão ou passará a consulta para o aplicativo de pesquisa registrado.

Os usuários podem usar a [sintaxe de consulta avançada](-search-2x-wds-aqsreference.md) para consultar o catálogo de mais eficientemente, controlando o escopo das pesquisas e combinando parâmetros de pesquisa com operadores boolianos. Por exemplo, um usuário pode pesquisar um anexo em um email de João que inclui "cronograma do projeto" ou "plano do projeto" com uma consulta semelhante à seguinte: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisitos de compatibilidade

O WDS 2.6.5 está disponível apenas para Windows 2000, Windows Server 2003 e Windows XP. O WDS é um download separado disponível da Microsoft gratuitamente para uso pessoal e comercial. Ele deve ser instalado e em uso para indexar a conta de usuário antes que os aplicativos criados para o WDS 2.6.5 funcionem.

### <a name="system-requirements"></a>Requisitos do Sistema

Os itens a seguir são necessários para usar o Windows Desktop Search:

-   Windows Internet Explorer ou posterior.
-   Para incluir suas mensagens de email no catálogo, você deve ter o Microsoft Microsoft Outlook 2000 ou posterior ou o Microsoft Outlook Express 6,0 ou posterior.
-   A visualização completa dos documentos do Microsoft Microsoft Office na exibição de resultados requer o Office XP ou posterior.
-   Processador Pentium 500 MHz mínimo (1 GHz recomendado).
-   Windows XP, Windows 2000 SP4 ou posterior ou Windows Server 2003 Service Pack 1.
-   Mínimo de 128 MB de RAM (recomenda-se 256 MB).
-   500 MB de espaço livre em disco rígido recomendado. O tamanho do índice depende da quantidade de conteúdo indexado.
-   resolução de tela de 1024 x 768 recomendada.

## <a name="related-topics"></a>Tópicos Relacionados

1.  Consultando o índice

    -   [Chamando o WDS de forma programática (via ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
    -   [Chamando o WDS por meio da linha de comando](-search-2x-wds-fromcommandline.md)

2.  [Estendendo o índice (visão geral)](-search-2x-wds-extendingtheindex.md)

    -   [Desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)

3.  Referências gerais

    -   [Esquema do WDS](-search-2x-wds-schematable.md)
    -   [Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
    -   [Tipos percebidos pelo WDS](-search-2x-wds-perceivedtype.md)

 

 