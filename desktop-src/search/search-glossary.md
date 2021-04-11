---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Glossário do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac0620f4c85c43aac6d41300e16e3e5a8dd037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090046"
---
# <a name="windows-search-glossary"></a>Glossário do Windows Search

## <a name=""></a>\#

**arquivo. OSD**

Arquivo do descritor de OpenSearch.

**arquivo. osdx**

Um arquivo XML de descrição de OpenSearch que descreve as conexões de servidor disponíveis e os formatos de resultado para uma fonte de dados específica baseada na Web. Ele é usado para interagir com o Shell do Windows. Consulte também: descritor de OpenSearch.

## <a name="a"></a>Um

**Sintaxe de consulta avançada (AQS)**

A sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa. O AQS é voltado principalmente para o usuário e pode ser usado por usuários para criar consultas AQS, mas também pode ser usado programaticamente. Consulte também: sintaxe de consulta natural (NQS).

**AQS**

Consulte a definição de: sintaxe de consulta avançada (AQS).

**associação**

Um mapeamento de uma extensão de nome de arquivo (por exemplo,. mp3) ou protocolo (por exemplo, http) para um identificador programático (ProgID). Esse mapeamento é armazenado no registro como uma configuração por usuário com um fallback por computador. Os aplicativos que participam do sistema de programas padrão definem o mapeamento de associação para a extensão de nome de arquivo ou protocolo para apontarem para as chaves ProgID que eles possuem.

**matriz de associação**

Uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo. Por exemplo, um arquivo. jpg tem a seguinte matriz de associação em um sistema Windows padrão: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "a \\ \\ imagem de SystemFileAssociations de HKCR", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Um esquema XML usado para Web feeds e distribuição de conteúdo, desenvolvido como uma alternativa ao RSS (Really Simple Syndication). O formato de distribuição Atom foi publicado como um padrão proposto pela IETF no RFC 4287.

## <a name="b"></a>B

**bind**

Para carregar ou associar código a dados. Por exemplo, um manipulador pode ser associado a uma fonte de dados do Shell.

**vinculação**

Uma solicitação em uma consulta de pesquisa para uma coluna em um conjunto de linhas retornado. A associação especifica uma propriedade a ser incluída nos resultados da pesquisa.

**bookmark**

Um indicador que identifica exclusivamente uma linha dentro de um conjunto de linhas.

## <a name="c"></a>C

**nome canônico**

O nome exclusivo de um recurso. Canônico significa "de acordo com as regras". Consulte também: nome do verbo canônico.

**nome do verbo canônico**

Um nome com neutralidade de idioma que pode ser usado programaticamente para se referir a um verbo, independentemente da cadeia de caracteres localizada na interface do usuário. Consulte também: nome canônico, verbo.

**catalog**

A unidade de nível mais alto da organização no Windows Search. Um catálogo representa um conjunto de documentos indexados que podem ser consultados. Um catálogo consiste em uma tabela de propriedades com o texto ou o valor e o local correspondente armazenado em colunas da tabela. Cada linha da tabela corresponde a um documento separado no escopo do catálogo, e cada coluna da tabela corresponde a uma propriedade. Consulte também: índice, serviço de pesquisa do Windows.

**category**

Um agrupamento hierárquico de linhas. Por exemplo, um resultado de consulta que contém colunas de autor e título pode ser categorizado com base no autor. Neste exemplo, cada grupo de linhas que contém o mesmo valor para o autor constitui uma categoria.

**6**

Uma coleção de linhas dentro de um conjunto de linhas. Consulte também: catálogo, categoria.

**column**

O contêiner para um único tipo de informação em uma linha. As colunas são mapeadas para nomes de propriedade e especifica quais propriedades são usadas para os elementos de árvore de comando da consulta de pesquisa. Consulte também: categoria.

**árvore de comandos**

Uma combinação de restrições, categorias e ordens de classificação que são especificadas para a consulta de pesquisa. Consulte também: categoria.

**contêiner**

Um tipo de item de shell que pode conter outros itens. Os itens em um contêiner são expostos ao namespace do shell usando uma fonte de dados do Shell. Os exemplos incluem pastas, unidades, servidores de rede e arquivos compactados com uma extensão de nome de arquivo. zip. Consulte também: fonte de dados do Shell, pasta, item de Shell.

**content**

Texto e propriedades associados a um item de shell ou a uma fonte de conteúdo que pode ser indexada.

**fonte de conteúdo**

Um item que pode ser acessado pelo indexador. As fontes de conteúdo são endereçáveis por uma URL e são fornecidas ao indexador por um manipulador de protocolo. Os exemplos incluem: arquivos e pastas do sistema de arquivos, itens e pastas do Microsoft Outlook, registros de banco de dados e itens armazenados do Microsoft SharePoint. Uma fonte de conteúdo pode ser exposta como itens de shell implementando uma fonte de dados do Shell. Consulte também: conteúdo, item de Shell.

**content view (exibição de conteúdo)**

Uma exibição no Windows Explorer (oferecida no Windows 7 e posterior) que exibe o conteúdo mais relevante para cada item da lista com base em sua associação de tipo ou extensão de nome de arquivo. A exibição de conteúdo usa uma lógica de redimensionamento que descarta Propriedades quando o tamanho da janela diminui para garantir que as propriedades mais críticas ainda tenham espaço para serem legíveis. Consulte também: padrão de layout, tipo, associação de tipo.

**modo de exibição de conteúdo**

Confira definição para: exibição de conteúdo.

**menu de contexto**

Esse termo às vezes é usado para significar o menu de atalho. Consulte definição para: menu de atalho.

**manipulador de menu de contexto**

Esse termo às vezes é usado para significar o manipulador de menu de atalho. Consulte a definição de: manipulador de menu de atalho.

**rastreamento**

Para iterar em um escopo de rastreamento, identificando as fontes de conteúdo que exigem indexação ou reindexação.

**escopo do rastreamento**

Uma coleção de armazenamentos de dados (identificável por URL) que representa o conteúdo que o indexador rastreia e indexa.

**cursor**

No contexto do índice local, um cursor é um indicador para trabalhar com uma linha ou um pequeno bloco de linhas por vez em um conjunto de dados retornado em um conjunto de resultados. Depois que o cursor é posicionado em uma linha, as operações podem ser executadas nessa linha ou em um bloco de linhas que começam nessa posição.

## <a name="d"></a>D

**Gerenciamento de Dados, exploração e mineração**

Consulte definição para: DMX (extensões de mineração de banco de dados).

**manipulador de objeto de dados**

Um manipulador que fornece formatos de área de transferência adicionais para o objeto de dados (IDataObject) de um item. Os objetos de dados são usados nos cenários de arrastar e soltar e copiar/colar.

**fonte de dados**

Esse termo às vezes é usado para significar o armazenamento de dados ou a fonte de dados do Shell. Consulte definição para: armazenamento de dados, fonte de dados do Shell.

**armazenamento de dados**

Um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação do shell como um contêiner usando uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.

**DMX (extensões de mineração de banco de dados)**

Uma linguagem de consulta usada para criar e manipular Data Mining. Os modelos administrativos do Windows 7, do Windows Search e do Windows Explorer são arquivos. admx e contam com a tecnologia DMX. Os modelos a seguir podem ser personalizados por meio de Política de Grupo: Search. admx, Explorer. admx e WindowsExplorer. admx.

**Symmetrix**

Consulte definição para: extensões de mineração de banco de dados.

**document**

Um item de shell que contém texto e para o qual a interface IFilter poderia ser implementada.

**descartar manipulador**

Um manipulador que permite que um determinado tipo de item dê suporte a cenários de arrastar e soltar e copiar/colar.

**soltar destino**

Um objeto de dados que é arrastado e descartado em um arquivo. Consulte também: manipulador de dados, descartar manipulador.

**verbo dinâmico**

Um verbo que depende do estado de um item de shell ou do sistema; a aparência do item é baseada em estado e requer que o código de execução determine se o item deve aparecer. Consulte também: manipulador de menu de atalho, verbo estático, verbo.

## <a name="e"></a>E

**Comando do Explorer**

Um objeto que pode ser apresentado como um botão próximo à parte superior da janela do Windows Explorer que fornece funcionalidade para itens e contêineres nessa janela. Uma fonte de dados do Shell fornece os objetos de comando do Windows Explorer para um item de contêiner específico. Os comandos às vezes são usados como verbos.

## <a name="f"></a>F

**pesquisa federada**

Um modelo de extensibilidade que permite pesquisar armazenamentos de dados e representar os resultados como itens de Shell no Windows Explorer. Consulte também: provedor de pesquisa federada, conector de pesquisa, descritor de OpenSearch, padrão OpenSearch.

**conector de pesquisa federada**

Consulte a definição para: conector de pesquisa.

**provedor de pesquisa federada**

Um serviço Web, implementado por um armazenamento de dados, que dá suporte aos protocolos usados pelo Windows 7 para que o Windows 7 e versões posteriores possam Pesquisar o armazenamento de dados remotamente. Consulte também: descritor de OpenSearch, OpenSearch Standard.

**Associação de arquivo**

Consulte a definição para: Associação de tipo de arquivo.

**formato de arquivo**

Um formato para dados armazenados em um arquivo que tem uma especificação de formato documentado. Os exemplos incluem o OLE DOCFILE, OPC, XML, ZIP e outras especificações de formato de arquivo conhecidas. Os criadores de tipo de arquivo geralmente usam um formato de arquivo existente como a base de um novo tipo de arquivo. Um formato de arquivo pode ser simplesmente uma definição que não é instanciada como um tipo de arquivo.

**manipulador de formato de arquivo**

Este termo é um sinônimo para o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

**extensão de nome de arquivo**

Consulte definição para: extensão de nome de arquivo.

**extensão de nome de arquivo**

O indicador principal de um tipo de arquivo para itens do sistema de arquivos, é a parte do nome do arquivo que segue o ponto final. A extensão de nome de arquivo não pode conter espaços ou caracteres não ASCII e aplica-se somente a arquivos (não pastas). As extensões de nome de arquivo são comparadas usando uma função de comparação que não é sensível ao caso ou à localidade. Consulte também: formato de arquivo, tipo de arquivo.

**tipo de arquivo**

Um valor de extensão de nome de arquivo específico, como ". htm" ou ". jpg", que define uma classe de arquivos que são do mesmo tipo e têm um conjunto comum de associações. Consulte também: tipo, associação de tipo de arquivo.

**associação de tipo de arquivo**

Para uma extensão de nome de arquivo específica, os elementos da matriz de associação que definem onde os manipuladores e outros atributos podem ser registrados. Consulte também: matriz de associação, tipo de arquivo.

**personalização de tipo de arquivo**

Uma associação que habilita o Shell a personalizar como o Shell trata um tipo de arquivo. As personalizações de tipo de arquivo incluem: especificar o aplicativo usado para abrir o arquivo quando clicado duas vezes, adicionando comandos ao menu de atalho para um tipo de arquivo, especificando um ícone personalizado, especificando um tipo de conteúdo MIME para associar a um tipo de arquivo, especificando um tipo percebido e especificando um ou mais aplicativos associados por tipo de arquivo com a caixa de diálogo abrir com. Consulte também: Percebidotype.

**manipulador de tipo de arquivo**

Um manipulador registrado para um tipo de arquivo. Consulte também: manipulador.

**filter**

Uma implementação da interface IFilter. Ele abre arquivos de um tipo de arquivo específico e filtra as propriedades e partes do texto do indexador. Os filtros são associados a tipos de arquivo, como indicado pelas extensões de nome de arquivo, tipos de MIME ou identificadores de classe (CLSIDs). Embora um filtro possa lidar com vários tipos de arquivo, cada tipo de arquivo funciona com apenas um filtro.

**pasta**

Consulte a definição para: contêiner.

## <a name="h"></a>H

**cliques**

Um objeto COM que fornece funcionalidade para um item de Shell. A maioria das fontes de dados de shell oferece um sistema extensível para ligar manipuladores a itens. Por exemplo, a pasta sistema de arquivos usa o sistema de associação para pesquisar os manipuladores de um determinado tipo de arquivo. Consulte também: Associação de arquivo, tipo de arquivo, personalização de tipo de arquivo.

## <a name="i"></a>I

**manipulador de ícone**

Um manipulador que fornece as informações necessárias para gerar e armazenar em cache um ícone para um item. O armazenamento de dados do sistema de arquivos dá suporte ao carregamento de um manipulador de ícones para um item com base no tipo de arquivo, permitindo que esse manipulador forneça um ícone que é usado para todas as instâncias desse tipo de arquivo.

**index**

n. Um catálogo que armazena o conteúdo e as propriedades de itens de Shell para habilitar pesquisas rápidas. Consulte também: catálogo, indexador, indexação, índice invertido. V. Para acessar as fontes de conteúdo, filtre as fontes de conteúdo e propriedades e insira os valores extraídos no índice (para texto) e no repositório de propriedades de pesquisa do Windows (para propriedades). Consulte também: fonte de conteúdo, índice, indexador, índice invertido.

**indexador**

Um aplicativo que faz indexação ou coordena a indexação. Consulte também: índice, indexação, índice invertido.

**manipulador InfoTip**

Um manipulador que fornece texto pop-up quando o usuário passa o ponteiro do mouse sobre um objeto da interface do usuário.

**índice invertido**

Uma estrutura persistente que contém o conteúdo extraído de arquivos pelo Windows Search. O texto é organizado em um índice que mapeia de uma palavra em uma propriedade para uma lista de documentos e locais dentro de um documento que contém essa palavra. Portanto, um índice invertido é o inverso do processo de extrair o texto e as propriedades do documento e colocá-los no indexador. Consulte também: index, indexer, indexação.

**item**

Consulte a definição de: item de Shell.

**classe de item**

Consulte definição para: tipo de arquivo.

## <a name="k"></a>K

**Tipo**

Uma propriedade que fornece um nome de tipo amigável e pode ser associada a uma lista de propriedades e um padrão de layout. O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo para o usuário final e foi definido como uma propriedade de cadeia de caracteres com vários valores (valores de cadeia de caracteres canônicos), assim, você pode ter um valor de tipo de "áudio; vídeo" ou "vincular; documento". Alguns nomes de tipos amigáveis do usuário já estão associados a propriedades e padrões de layout. Por exemplo, itens associados ao tipo. imagem e itens associados a Kind.Document exibem propriedades diferentes mesmo quando estão na mesma exibição. Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout. Consulte também: espécie de associação, exibição de conteúdo, padrão de layout.

**Associação de tipo**

Uma propriedade no sistema de propriedades, chamada System. Kind, que determina quais modelos de UX são exibidos para um arquivo. Essa propriedade também fornece um nome amigável para o tipo de item e está vinculado à extensão de nome de arquivo. Consulte também: Kind.

## <a name="l"></a>L

**padrão de layout**

Uma das várias disposições para exibir propriedades. No Windows 7 e posterior, ao registrar um novo tipo de arquivo, você pode usar a exibição de conteúdo para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo. Você pode escolher entre quatro padrões de layout diferentes: alfa (para resultados de pesquisa de documentos que contêm trechos de código), beta (para resultados de pesquisa de email com trechos de código), gama (semelhante a alfa, mas com um layout de duas linhas em vez de quatro) e Delta (para mostrar muitas propriedades mais curtas, como com música e imagens). Consulte também: exibição de conteúdo, tipo, associação de tipo.

## <a name="m"></a>M

**manipulador de metadados**

Esse termo às vezes é usado para significar o manipulador de propriedades. Consulte a definição de: manipulador de propriedade.

## <a name="n"></a>N

**extensão do namespace**

Consulte a definição de: fonte de dados do Shell.

**movimentação do namespace**

Um processo auxiliar que percorre o namespace de um contêiner ou conjunto de contêineres, descobrindo cada item e possivelmente fazendo algo com cada um. A interface INamespaceWalk pode ser usada para percorrer qualquer parte do namespace do Windows Explorer ou para descobrir os itens referenciados por um objeto de dados ou uma exibição. Os verbos de contêiner (como "Play" nos contêineres artistas) orientam o namespace e descobrem os itens.

**consulta de linguagem natural**

Consulte a definição de: sintaxe de consulta natural (NQS).

**Sintaxe de consulta natural (NQS)**

Uma sintaxe de consulta que é mais relaxada do que AQS e é mais parecida com a linguagem humana. NQS pode ser usado pelo Windows Search para consultar o índice se NQS for selecionado em vez do padrão, AQS. Consulte também: sintaxe de consulta avançada (AQS).

**palavra de ruído**

Uma palavra que é ignorada pelo Windows Search quando está presente nas restrições especificadas para a consulta de pesquisa, pois ela tem pouco valor de discriminador. Os exemplos incluem "and" e "The."

**NQS**

Consulte a definição de: sintaxe de consulta natural (NQS).

## <a name="o"></a>O

**Banco de dados de vinculação e incorporação de objetos (OLE DB)**

Um conjunto padrão de interfaces que fornece acesso heterogêneo a fontes diferentes de informações localizadas em qualquer lugar, como sistemas de arquivos, pastas de email e bancos de dados.

**OLE DB**

Consulte definição para: vinculação de objetos e banco de dados de incorporação.

**Descritor de OpenSearch**

Um arquivo XML que descreve as conexões de servidor disponíveis e os formatos de resultado para uma fonte de dados específica baseada na Web. Esse arquivo contém um ou mais modelos de URL e usa uma extensão de nome de arquivo. osdx ao interagir com o Shell do Windows. Algumas vezes, uma descrição de OpenSearch é chamada de conector de pesquisa, embora seja apenas a parte de descrição de um conector. Consulte também: conector de pesquisa.

**Padrão OpenSearch**

Uma coleção de formatos e protocolos simples usados para compartilhar resultados de pesquisa. Para obter mais informações, consulte o site do OpenSearch ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Uma categoria ampla de tipos de formato de arquivo. O percebidatype foi introduzido no Windows XP e dá suporte a um conjunto limitado de tipos de arquivo conhecidos (exemplos incluem imagem, texto, áudio e tipos de arquivo compactados). Tipos de arquivo, geralmente tipos de arquivo públicos, também podem ter um tipo percebido. Por exemplo, o arquivo de imagem Types. bmp,. png,. jpg e. gif também são do tipo percebido, Image. Na camada de programação, Percebidotype é expresso como um inteiro. Como há código que usa tipo e Percebidotype, os proprietários de formato de arquivo devem registrar ambos. Por exemplo, "reproduzir tudo" depende de Percebidotype. Consulte também: tipo de arquivo.

**Gerenciador de visualização**

Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item de Shell a ser exibido no painel de visualização do Windows Explorer.

**pré-visualizador**

Esse termo às vezes é usado para significar o Gerenciador de visualização. Consulte a definição para: Gerenciador de visualização.

**manipulador de propriedades**

Um manipulador que traduz dados armazenados em um arquivo em um esquema estruturado que é reconhecido pelo e pode ser acessado pelo Windows Explorer, pelo Windows Search e por outros aplicativos. Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para o arquivo. Os dados traduzidos incluem exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante. Cada manipulador de propriedade é associado a um tipo de arquivo específico, identificado pela extensão de nome de arquivo. Consulte também: sistema de propriedades.

**manipulador de folhas de propriedades**

Um manipulador que é usado para criar folhas de propriedades personalizadas com imagens e controles da interface do usuário que permitem a interação personalizada com um tipo de arquivo.

**sistema de propriedades**

Um sistema de leitura/gravação extensível de definições de dados que usa propriedades implementadas como pares de nome-valor. Consulte também: manipulador de propriedades, item de Shell.

**valor da propriedade**

Um valor associado a um nome de propriedade para um item de Shell. Por exemplo, "autor", "tamanho" e "data de uso" são propriedades. Os valores de propriedade são expressos como uma estrutura PROPVARIANT.

**manipulador de protocolo**

Um manipulador que acessa fontes de conteúdo e fornece um objeto IUrlAccessor para um protocolo e uma URL especificados. Os manipuladores de protocolo estendem a funcionalidade de pesquisa do Windows e podem fornecer notificações de alteração aos indexadores. Manipuladores de protocolo diferentes são necessários para indexar tipos específicos de armazenamentos de dados. Para fornecer uma experiência de usuário razoável, você também deve fornecer uma fonte de dados do Shell para o armazenamento de dados, além de implementar seu manipulador de protocolo. O manipulador de protocolo expõe os itens no armazenamento de dados para o indexador, enquanto a fonte de dados do Shell expõe os itens no armazenamento de dados para o Shell.

## <a name="r"></a>R

**Elas**

Uma condição que um arquivo deve atender para ser incluído nos resultados da pesquisa que são retornados pelo Windows Search.

**row**

As colunas que contêm os valores de propriedade que descrevem um único resultado do conjunto de objetos que corresponderam às restrições especificadas em uma consulta de pesquisa.

**linhas**

Um conjunto de linhas retornadas nos resultados da pesquisa.

## <a name="s"></a>S

**conector de pesquisa**

Um arquivo XML que contém informações sobre um armazenamento de dados. Os conectores de pesquisa são implantados para pesquisa federada.

**Pesquisar consumidor**

Um componente ou aplicativo que consulta o índice.

**Pesquisar Federação**

Consulte a definição para: provedor de pesquisa federada.

**provedor de pesquisa**

Um componente ou aplicativo que fornece dados para o Windows Search.

**escopo da pesquisa**

Esse termo às vezes é usado para significar o escopo do rastreamento. Consulte definição para: escopo do rastreamento.

**Fonte de dados do Shell**

Um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados. No passado, a fonte de dados do Shell era chamada de extensão de namespace do Shell. Consulte também: contêiner, manipulador, item de Shell.

**Extensão do shell**

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

**Manipulador de extensão de Shell**

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

**Manipulador de Shell**

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

**Item do Shell**

Uma única parte do conteúdo. Alguns itens de shell são fontes de conteúdo e outros não. Uma pasta é uma fonte de conteúdo, por exemplo, mas um arquivo. jpg não é. Manipuladores de tipo de arquivo expõem itens de Shell. Em alguns contextos, "item" é usado para distinguir contêineres de não contidos. Consulte também: contêiner, fonte de conteúdo, manipulador de tipo de arquivo.

**Extensão do namespace do Shell**

Esse termo às vezes é usado para significar a fonte de dados do Shell. Consulte a definição de: fonte de dados do Shell.

**menu de atalho**

Uma interface do usuário que é usada para apresentar uma coleção de verbos associados a um elemento de interface do usuário, como um arquivo ou uma pasta.

**Manipulador de menu de atalho**

Um manipulador que adiciona verbos para um item ou itens. Esses verbos são normalmente exibidos em um menu de atalho. Consulte também: menu de atalho.

**verbo estático**

Um verbo que se aplica a um item de shell sem a necessidade de inspecionar o estado atual de um item ou sistema. Um verbo estático é baseado em um registro estático dos elementos associados de um item e não é alterado.

## <a name="t"></a>T

**manipulador de miniaturas**

Um manipulador que fornece uma imagem estática para representar um item de Shell.

**provedor de miniatura**

Esse termo às vezes é usado para significar o manipulador de miniaturas. Consulte a definição de: manipulador de miniatura.

## <a name="u"></a>U

**Modelo do URL**

Uma cadeia de conexão baseada em URL que é usada para consultar um servidor Web para resultados da pesquisa. O modelo é semelhante a uma URL, mas contém vários valores de espaço reservado (como {searchTerms}) que o cliente deve substituir por dados sobre os resultados que deseja recuperar. A definição de modelos de URL é a chave para implementar os padrões de pesquisa federada e OpenSearch.

**nome de tipo amigável do usuário**

Consulte a definição de: Kind.

## <a name="v"></a>V

**verbo**

Uma ação individual que pode ser chamada por um item de Shell. Os exemplos incluem abrir e imprimir. Os verbos são, às vezes, chamados de comandos ou tarefas. Consulte também: verbo dinâmico, manipulador de menu de atalho, verbo estático.

**manipulador de verbo**

Esse termo às vezes é usado para significar o manipulador de menu de atalho. Consulte a definição de: manipulador de menu de atalho.

## <a name="w"></a>W

**corre**

Consulte a definição para: passo de namespace.

**Windows Search**

Consulte a definição para: serviço de pesquisa do Windows.

**Repositório de propriedades de pesquisa do Windows**

O cache dos valores de propriedade usados na implementação do serviço de pesquisa do Windows. Esses valores de propriedade podem ser consultados programaticamente usando o provedor de OLE DB do Windows Search. O armazenamento de propriedades de pesquisa do Windows coleta e armazena as propriedades emitidas por manipuladores de filtro ou manipuladores de propriedade quando um item como um documento do Word é indexado. Esse armazenamento é Descartado e recriado quando o índice é recriado.

**Serviço de pesquisa do Windows**

Refere-se ao Windows Search 3,0 e superior. Esse serviço analisa um conjunto de documentos, extrai informações úteis e, em seguida, organiza as informações extraídas para que as propriedades desses documentos possam ser retornadas de forma eficiente em resposta a consultas. Consulte também: catálogo.
