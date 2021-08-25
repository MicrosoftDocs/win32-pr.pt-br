---
title: Windows Pesquisa de Área de Trabalho 2.x
description: Entenda Windows Desktop Search 2.x. Para Windows versões posteriores Windows XP e Windows Server 2003, use Windows Search.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3298d668266d913a427c74f605435257c1a4cfba56fae82c809bd9127e7ecf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829096"
---
# <a name="windows-desktop-search-2x"></a>Windows Pesquisa de Área de Trabalho 2.x

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

O uso do e do desenvolvimento para as versões 2.x do WDS (Pesquisa de Área de Trabalho) do Microsoft Windows é fortemente desacentado em favor [do Windows Search](../search/-search-3x-wds-overview.md).

O WDS é um serviço de indexação e uma plataforma que fornece uma pesquisa rápida de arquivos e dados em diferentes fontes de dados e locais. O WDS ajuda os usuários e outros aplicativos a encontrar quase tudo em seus computadores, mensagens de email, compromissos de calendário, fotos, documentos e muito mais. Além disso, o WDS pode retornar resultados de várias fontes de dados em um ambiente do Windows Explorer para que os usuários possam visualizar, filtrar e agir rapidamente nos resultados da pesquisa.

O WDS indexa dados dentro de um determinado escopo de rastreamento, os locais especificados em um computador local e a rede compartilhada que o Indexador deve rastrear. Esse escopo de rastreamento pode ser controlado por opções de conjunto de usuários, APIs de gerenciamento e Políticas de Grupo, que os administradores de rede podem configurar para controlar as permissões de acesso do usuário e as configurações de indexação. As Políticas de Grupo podem restringir o acesso a determinados recursos de rede, bem como definir recursos a serem indexados.

Esta seção contém os seguintes tópicos:

-   [Visão geral](#windows-desktop-search-2x)
    -   [Sobre o Indexador do WDS](#about-the-wds-indexer)
    -   [Sobre o catálogo do WDS](#about-the-wds-catalog)
    -   [Sobre o Mecanismo de Pesquisa e os Resultados](#about-the-search-engine-and-results)
-   [Desenvolvendo com o WDS](#developing-with-wds)
    -   [Adicionando dados ao índice com complementos](#adding-data-to-the-index-with-add-ins)
    -   [Consultando o índice](#querying-the-index)
-   [Requisitos de compatibilidade](#compatibility-requirements)
    -   [Requisitos do sistema](#system-requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

### <a name="about-the-wds-indexer"></a>Sobre o Indexador do WDS

Quando instalado pela primeira vez, o Indexador rastrea os arquivos mais comuns voltados para o usuário na pasta Meus Documentos, pastas de email do Microsoft Outlook e Microsoft Outlook Express e locais especificados no Política de Grupo. Os usuários também podem especificar novos arquivos e locais para o Indexador incluir (ou excluir) em rastreamentos sucessivos. Cada local incluído é identificado por URL e o Indexador começará nessa URL e iterará recursivamente por subpastas ou locais até que todos os itens tenham sido indexados. Um escopo é um conjunto de URLs. As APIs de gerenciamento podem ser usadas por aplicativos personalizados para definir seu escopo de rastreamento, um conjunto de URLs apontando para caminhos dentro de um protocolo, como para pastas em uma unidade ou para armazenamentos de email MAPI como `file://` `mapi:// ` Outlook. O WDS usa manipuladores de protocolo para acessar os armazenamentos de dados e filtros para analisar e indexar o texto e as propriedades dos itens. Esses dados são armazenados no catálogo.

### <a name="about-the-wds-catalog"></a>Sobre o catálogo do WDS

O catálogo do WDS é um índice de texto e propriedades coletados de itens no email especificado, unidades locais, recursos de rede e outros armazenamentos de dados locais. O conteúdo do catálogo se baseia em opções e regras definidas pelo WDS, aplicativos baseados na plataforma WDS, preferências de usuário e políticas de grupo. Há mais de 200 propriedades disponíveis para cada item indexado, como data de criação, tamanho e propriedades específicas do tipo ("De" para mensagens de email). Para ver uma lista dessas propriedades, consulte Referência de [esquema](-search-2x-wds-schematable.md)WDS .

### <a name="about-the-search-engine-and-results"></a>Sobre o Mecanismo de Pesquisa e os Resultados

Na barra de mesa do WDS ou do Windows Explorer, os usuários podem pesquisar o conteúdo de texto completo e os metadados de propriedade de itens indexados. Os mesmos tipos de pesquisas também podem ser iniciados da linha de comando, de uma página da Web ou de um aplicativo personalizado. O Mecanismo de Pesquisa do WDS localiza itens correspondentes aos critérios de pesquisa e os retorna como conjuntos de resultados do Microsoft ActiveX Data Objects (ADO). O WDS exibe itens correspondentes aos critérios de pesquisa e pode apresentar uma visualização rica do item. Você pode criar aplicativos para interceptar a consulta de pesquisa, executar a pesquisa e/ou exibir o conjunto de resultados.

## <a name="developing-with-wds"></a>Desenvolvendo com o WDS

Há dois tipos principais de integração com o WDS: adicionar dados ao índice e consultar o conteúdo do índice para recuperar registros correspondentes aos critérios de pesquisa.

### <a name="adding-data-to-the-index-with-add-ins"></a>Adicionando dados ao índice com Add-Ins

Há basicamente dois tipos de fontes de dados: armazenamentos do sistema de arquivos e armazenamentos de sistema que não são arquivos. Um grupo de arquivos no Meus Documentos é um armazenamento de sistema de arquivos simples. O WDS poderá pesquisar informações nos arquivos armazenados em um sistema de arquivos desse tipo se puder localizar um filtro para o tipo de arquivo. Você poderá habilitar o WDS para indexar um novo tipo de arquivo proprietário se fornecer uma implementação da interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para esse tipo de arquivo.

Um armazenamento de sistema que não é de arquivos, como um banco de dados, requer um manipulador de protocolo para permitir que o WDS navegue e indexe dados no armazenamento de dados. Por exemplo, se você tiver um cliente de email que armazena sua lista de emails recebidos em seu próprio arquivo (como arquivos PST no Outlook), poderá fornecer um manipulador de protocolo para indexar e pesquisar cada email individual fornecendo um manipulador de protocolo. Se o armazenamento de dados for hierárquico, você também precisará implementar uma interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para enumerar os itens no armazenamento. Para uma melhor experiência do usuário, você pode implementar uma Extensão do Shell para fornecer menus de contexto e ícones de dentro da exibição de resultados.

Atualmente, o WDS contém filtros para mais de 200 tipos de itens (incluindo itens de texto não criptografado, como arquivos HTML, XML e código-fonte) e usa a mesma tecnologia de manipulador de protocolo e [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Se você já tiver filtros instalados para tipos de arquivo proprietários, o WDS poderá usar as interfaces de filtro existentes para indexar esses dados.

### <a name="querying-the-index"></a>Consultando o índice

O WDS fornece aplicativos com conjuntos de resultados personalizados de dados do índice com base em qualquer um dos valores de esquema disponíveis. Os resultados são retornados como conjuntos de registros ADO. Há quatro maneiras de incorporar consultas WDS em um aplicativo, cada uma oferecendo vários níveis de personalização e robustez.

-   Interface ISearchDesktop – AS APIs nessa interface são usadas para chamar o WDS programaticamente especificando uma cadeia de caracteres de consulta, uma lista de colunas a retornar, restrições de escopo semelhantes a uma cláusula WHERE linguagem SQL (SQL) e o nome da coluna a ser classificação. Essas APIs estão disponíveis para código nativo e gerenciado.
-   Controle de ActiveX WDS – esse controle desenha a interface de pesquisa do WDS e gerencia a pesquisa e a exibição de resultados. Esse método é mais fácil do que usar as APIs, mas é menos flexível. Para usar esse controle em um aplicativo  Microsoft Visual Studio, acesse a caixa de diálogo Escolher Itens da Caixa de Ferramentas  no **menu** Ferramentas e adicione "Pesquisa de Área de Trabalho do Windows – Visualizador de Resultados" à Caixa de Ferramentas da guia Componentes **COM.** Em seguida, adicione o controle ao formulário em que você deseja incluí-lo. O controle ActiveX WDS é compatível apenas com o WDS 2.x e 3.x Windows XP.
-   Parâmetros de linha de comando – os aplicativos podem chamar o executável do WDS com vários parâmetros para pesquisar e exibir resultados. Isso abrirá uma janela do WDS com os resultados exibidos. Essa é a maneira mais fácil de adicionar a pesquisa a um aplicativo, mas não retorna ao aplicativo de chamada nenhuma informação sobre o que o usuário faz dentro da janela do WDS.
-   BHO (Objeto Auxiliar do Navegador WDS) – Da mesma forma, as páginas da Web podem usar o BHO para enviar consultas ao WDS ou ao aplicativo de pesquisa registrado. Depois de validar a URL de páginas da Web em relação à lista de segurança de domínio do WDS, o WDS executará a consulta e exibirá os resultados usando a interface de pesquisa padrão ou passará a consulta para o aplicativo de pesquisa registrado.

Os usuários podem usar [a](-search-2x-wds-aqsreference.md) Sintaxe de Consulta Avançada para consultar o catálogo com mais potência controlando o escopo de pesquisas e combinando parâmetros de pesquisa com operadores boolianas. Por exemplo, um usuário pode pesquisar um anexo em um email de João que inclui "agendamento de projeto" ou "plano de projeto" com uma consulta como a seguinte: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Requisitos de compatibilidade

O WDS 2.6.5 está disponível somente para Windows 2000, Windows Server 2003 e Windows XP. O WDS é um download separado disponível da Microsoft gratuitamente para uso pessoal e comercial. Ele deve ser instalado e em uso para indexar a conta de usuário antes que os aplicativos criado para o WDS 2.6.5 funcionem.

### <a name="system-requirements"></a>Requisitos do Sistema

Os seguintes são necessários para usar Windows Desktop Search:

-   Windows Internet Explorer ou posterior.
-   Para incluir suas mensagens de email no catálogo, você deve ter o Microsoft Microsoft Outlook 2000 ou posterior ou o Microsoft Outlook Express 6.0 ou posterior.
-   A visualização completa do Microsoft Microsoft Office documentos na exibição de resultados requer Office XP ou posterior.
-   Processador Mínimo pentium de 500 MHz (recomendado de 1 GHz).
-   Windows XP, Windows 2000 SP4 ou posterior ou Windows Server 2003 Service Pack 1.
-   Mínimo de 128 MB de RAM (recomendado de 256 MB).
-   Recomendamos 500 MB de espaço livre em disco rígido. O tamanho do índice depende de quanto conteúdo você indexou.
-   Resolução de tela 1024 x 768 recomendada.

## <a name="related-topics"></a>Tópicos relacionados

1.  Consultando o índice

    -   [Chamando o WDS programaticamente (por meio de ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Chamando o WDS de páginas da Web](-search-2x-wds-browserhelpobject.md)
    -   [Chamando o WDS da linha de comando](-search-2x-wds-fromcommandline.md)

2.  [Estendendo o índice (visão geral)](-search-2x-wds-extendingtheindex.md)

    -   [Desenvolvendo complementos de IFilter](-search-2x-wds-ifilteraddins.md)
    -   [Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)

3.  Referências gerais

    -   [Esquema do WDS](-search-2x-wds-schematable.md)
    -   [Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
    -   [Tipos percebidos pelo WDS](-search-2x-wds-perceivedtype.md)

 

 