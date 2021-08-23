---
description: Página do glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 8e9b45de-c81b-4324-b00b-b11ee6749920
title: Windows Glossário de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efe8bbe07badc7575cc3aba83100814d601bc5c8ebca24961b198950b2e5e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844646"
---
# <a name="windows-search-glossary"></a>Windows Glossário de pesquisa

## <a name=""></a>\#

**Arquivo .osd**

OpenSearch Arquivo do descritor.

**Arquivo .osdx**

Um OpenSearch XML de descrição que descreve as conexões de servidor disponíveis e os formatos de resultado para uma fonte de dados específica baseada na Web. Ele é usado para interagir com o shell Windows. Confira também: OpenSearch descritor.

## <a name="a"></a>Um

**Sintaxe de consulta avançada (AQS)**

A sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir parâmetros de pesquisa. O AQS é voltado principalmente para o usuário e pode ser usado por usuários para criar consultas do AQS, mas também pode ser usado programaticamente. Consulte também: NQS (Sintaxe de Consulta Natural).

**Aqs**

Consulte a definição de: AQS (Advanced Query Syntax).

**Associação**

Um mapeamento de uma extensão de nome de arquivo (por exemplo, .mp3) ou protocolo (por exemplo, http) para um ProgID (identificador programático). Esse mapeamento é armazenado no Registro como uma configuração por usuário com um fallback por computador. Os aplicativos que participam do sistema de Programas Padrão configuram o mapeamento de associação para a extensão de nome de arquivo ou protocolo para apontar para as chaves ProgID que eles têm.

**matriz de associação**

Uma lista ordenada de locais do Registro usada para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo. Por exemplo, um arquivo .jpg tem a seguinte matriz de associação em um sistema de Windows padrão: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\.jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

**Atom**

Um esquema XML usado para feeds da Web e distribuição de conteúdo, desenvolvido como uma alternativa ao RSS (Really Simple Syndication). O formato de sindicalização Atom foi publicado como um padrão proposto pelo IETF na RFC 4287.

## <a name="b"></a>B

**bind**

Para carregar ou associar código a dados. Por exemplo, um manipulador pode ser associado a uma fonte de dados do Shell.

**Ligação**

Uma solicitação em uma consulta de pesquisa para uma coluna em um conjuntos de linhas retornado. A associação especifica uma propriedade a ser incluída nos resultados da pesquisa.

**bookmark**

Um indicador que identifica exclusivamente uma linha dentro de um conjunto de linhas.

## <a name="c"></a>C

**nome canônico**

O nome exclusivo de um recurso. Canônico significa "de acordo com as regras". Consulte também: nome do verbo canônico.

**nome do verbo canônico**

Um nome neutro em idioma que pode ser usado programaticamente para se referir a um verbo, independentemente da cadeia de caracteres localizada na interface do usuário. Consulte também: nome canônico, verbo.

**catalog**

A unidade de nível mais alto da organização no Windows Search. Um catálogo representa um conjunto de documentos indexados que podem ser consultados. Um catálogo consiste em uma tabela de propriedades com o texto ou o valor e o local correspondente armazenado em colunas da tabela. Cada linha da tabela corresponde a um documento separado no escopo do catálogo e cada coluna da tabela corresponde a uma propriedade. Consulte também: index, Windows serviço Pesquisa.

**category**

Um grupo hierárquico de linhas. Por exemplo, um resultado de consulta que contém colunas de autor e título pode ser categorizado com base no autor. Neste exemplo, cada grupo de linhas que contém o mesmo valor para autor constitui uma categoria.

**Capítulo**

Uma coleção de linhas dentro de um conjunto de linhas. Confira também: catálogo, categoria.

**column**

O contêiner para um único tipo de informação em uma linha. As colunas são mapeadas para nomes de propriedade e especificam quais propriedades são usadas para os elementos da árvore de comandos da consulta de pesquisa. Confira também: categoria.

**árvore de comandos**

Uma combinação de restrições, categorias e ordens de classificação especificadas para a consulta de pesquisa. Confira também: categoria.

**contêiner**

Um tipo de item shell que pode conter outros itens. Os itens em um contêiner são expostos ao namespace do Shell usando uma fonte de dados do Shell. Os exemplos incluem pastas, unidades, servidores de rede e arquivos compactados com uma extensão .zip nome de arquivo. Confira também: Fonte de dados do shell, pasta, item shell.

**content**

Texto e propriedades associadas a um item shell ou uma fonte de conteúdo que pode ser indexada.

**fonte de conteúdo**

Um item que pode ser acessado pelo indexador. As fontes de conteúdo são acessível por uma URL e são fornecidas ao indexador por um manipulador de protocolo. Os exemplos incluem: arquivos e pastas do sistema de arquivos, Outlook e pastas da Microsoft, registros de banco de dados e SharePoint itens armazenados. Uma fonte de conteúdo pode ser exposta como itens do Shell implementando uma fonte de dados do Shell. Consulte também: conteúdo, item shell.

**content view (exibição de conteúdo)**

Uma exibição no Windows Explorer (oferecida no Windows 7 e posterior) que exibe o conteúdo mais relevante para cada item na lista com base em sua extensão de nome de arquivo ou associação de tipo. A exibição de conteúdo usa uma lógica de re tamanho que descarta propriedades quando o tamanho da janela diminui para garantir que as propriedades mais críticas ainda tenham espaço para serem claramente acessível. Confira também: padrão de layout, Tipo, Associação de tipo.

**modo de exibição de conteúdo**

Consulte definição para: exibição de conteúdo.

**menu de contexto**

Às vezes, esse termo é usado para significar o menu de atalho. Consulte a definição de: menu de atalho.

**manipulador de menu de contexto**

Às vezes, esse termo é usado para significar o manipulador de menu de atalho. Consulte definição para: manipulador de menu de atalho.

**rastreamento**

Para iterar em um escopo de rastreamento, identificando fontes de conteúdo que exigem indexação ou nova indexação.

**escopo de rastreamento**

Uma coleção de armazenamentos de dados (identificáveis por URL) que representa o conteúdo que o indexador rastrea e indexa.

**cursor**

No contexto do índice local, um cursor é um indicador para trabalhar com uma linha ou um pequeno bloco de linhas por vez em um conjunto de dados retornados em um conjunto de resultados. Depois que o cursor é posicionado em uma linha, as operações podem ser executadas nessa linha ou em um bloco de linhas começando nessa posição.

## <a name="d"></a>D

**Gerenciamento de Dados, exploração e mineração**

Consulte definição para: DMX (Extensões de Mineração de Banco de Dados).

**manipulador de objetos de dados**

Um manipulador que fornece formatos de área de transferência adicionais para o objeto de dados (IDataObject) de um item. Os objetos de dados são usados em cenários de arrastar e soltar e copiar/colar.

**fonte de dados**

Às vezes, esse termo é usado para significar o armazenamento de dados ou a fonte de dados do Shell. Consulte definição para: armazenamento de dados, fonte de dados do Shell.

**armazenamento de dados**

Um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação shell como um contêiner usando uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema Windows Search usando um manipulador de protocolo.

**DMX (Extensões de Mineração de Banco de Dados)**

Uma linguagem de consulta usada para criar e manipular a mineração de dados. Os modelos administrativos para Windows 7, Windows Search e Windows Explorer são arquivos .admx e dependem da tecnologia DMX. Os modelos a seguir podem ser personalizados por meio Política de Grupo: Search.admx, Explorer.admx e WindowsExplorer.admx.

**Dmx**

Consulte a definição de: Extensões de Mineração de Banco de Dados.

**document**

Um item shell que contém texto e para o qual a interface IFilter pode ser implementada.

**manipulador de soltar**

Um manipulador que habilita um tipo de item específico para dar suporte a cenários de arrastar e soltar e copiar/colar.

**drop target**

Um objeto de dados que é arrastado e descartado em um arquivo. Consulte também: manipulador de dados, manipulador de soltar.

**verbo dinâmico**

Um verbo que depende do estado de um item shell ou do sistema; a aparência do item é baseada em estado e exige que o código em execução determine se o item deve aparecer. Consulte também: manipulador de menu de atalho, verbo estático, verbo.

## <a name="e"></a>E

**Comando do Explorer**

Um objeto que pode ser apresentado como um botão próximo à parte superior da janela Windows Explorer que fornece funcionalidade para itens e contêineres nessa janela. Uma fonte de dados do Shell fornece os Windows de comando do Explorer para um item de contêiner específico. Às vezes, os comandos são usados como verbos.

## <a name="f"></a>F

**pesquisa federada**

Um modelo de extensibilidade que permite pesquisar armazenamentos de dados e representar os resultados como itens do Shell no Windows Explorer. Confira também: provedor de pesquisa federado, conector de pesquisa, OpenSearch descritor, OpenSearch padrão.

**federado search connector**

Consulte a definição de: search connector.

**provedor de pesquisa federada**

Um serviço Web, implementado por um armazenamento de dados, que dá suporte aos protocolos usados pelo Windows 7 para que Windows 7 e versões posteriores possam pesquisar remotamente esse armazenamento de dados. Confira também: OpenSearch descritor, OpenSearch padrão.

**associação de arquivo**

Consulte definição para: associação de tipo de arquivo.

**formato de arquivo**

Um formato para dados armazenados em um arquivo que tem uma especificação de formato documentada. Os exemplos incluem OLE DocFile, OPC, XML, ZIP e outras especificações de formato de arquivo conhecidas. Os criadores de tipo de arquivo geralmente usam um formato de arquivo existente como a base de um novo tipo de arquivo. Um formato de arquivo pode ser simplesmente uma definição que não é instautada como um tipo de arquivo.

**manipulador de formato de arquivo**

Esse termo é um sinônimo para o manipulador de tipo de arquivo. Consulte definição para: manipulador de tipo de arquivo.

**extensão de nome de arquivo**

Consulte definição para: extensão de nome de arquivo.

**extensão de nome de arquivo**

O indicador principal de um tipo de arquivo para itens do sistema de arquivos, é a parte do nome do arquivo que segue o ponto final. A extensão de nome de arquivo não pode conter espaços ou caracteres não ASCII e se aplica somente a arquivos (não a pastas). As extensões de nome de arquivo são comparadas usando uma função de comparação que não é sensível a minúsculas ou localidades. Consulte também: formato de arquivo, tipo de arquivo.

**tipo de arquivo**

Um valor de extensão de nome de arquivo específico, como ".htm" ou ".jpg", que define uma classe de arquivos que são do mesmo tipo e têm um conjunto comum de associações. Consulte também: Tipo, associação de tipo de arquivo.

**associação de tipo de arquivo**

Para uma extensão de nome de arquivo específica, os elementos da matriz de associação que definem onde manipuladores e outros atributos podem ser registrados. Consulte também: matriz de associação, tipo de arquivo.

**personalização de tipo de arquivo**

Uma associação que permite que o Shell personalize como o Shell trata um tipo de arquivo. As personalizações de tipo de arquivo incluem: especificar o aplicativo usado para abrir o arquivo quando clicado duas vezes, adicionar comandos ao menu de atalho para um tipo de arquivo, especificar um ícone personalizado, especificar um tipo de conteúdo MIME para associar a um tipo de arquivo, especificar um tipo percebido e especificar um ou mais aplicativos associados por tipo de arquivo com a caixa de diálogo Abrir com. Consulte também: PerceivedType.

**manipulador de tipo de arquivo**

Um manipulador registrado para um tipo de arquivo. Consulte também: manipulador.

**filter**

Uma implementação da interface IFilter. Ele abre arquivos de um tipo de arquivo específico e filtra propriedades e partes de texto para o indexador. Os filtros são associados a tipos de arquivo, conforme denotado por extensões de nome de arquivo, tipos MIME ou CLSIDs (identificadores de classe). Embora um filtro possa lidar com vários tipos de arquivo, cada tipo de arquivo funciona com apenas um filtro.

**Pasta**

Consulte a definição para: contêiner.

## <a name="h"></a>H

**handler**

Um objeto COM que fornece funcionalidade para um item do Shell. A maioria das fontes de dados do Shell oferece um sistema extensível para manipuladores de associação a itens. Por exemplo, a pasta do sistema de arquivos usa o sistema de associação para procurar os manipuladores de um tipo de arquivo específico. Confira também: associação de arquivo, tipo de arquivo, personalização de tipo de arquivo.

## <a name="i"></a>I

**manipulador de ícones**

Um manipulador que fornece as informações necessárias para gerar e armazenar em cache um ícone para um item. O armazenamento de dados do sistema de arquivos dá suporte ao carregamento de um manipulador de ícones para um item com base no tipo de arquivo, permitindo que esse manipulador forneça um ícone usado para todas as instâncias desse tipo de arquivo.

**index**

n. Um catálogo que armazena o conteúdo e as propriedades dos itens do Shell para habilitar pesquisas rápidas. Consulte também: catálogo, indexador, indexação, índice invertido. V. Para acessar fontes de conteúdo, filtre as fontes de conteúdo e propriedades e insira os valores extraídos no índice (para texto) e no armazenamento de propriedades Windows Search (para propriedades). Consulte também: fonte de conteúdo, índice, indexador, índice invertido.

**Indexador**

Um aplicativo que faz indexação ou coordena a indexação. Consulte também: índice, indexação, índice invertido.

**manipulador infotip**

Um manipulador que fornece texto pop-up quando o usuário passar o ponteiro do mouse sobre um objeto de interface do usuário.

**índice invertido**

Uma estrutura persistente que contém o conteúdo retirado dos arquivos Windows Search. O texto é organizado em um índice que mapeia de uma palavra em uma propriedade para uma lista de documentos e locais dentro de um documento que contém essa palavra. Portanto, um índice invertido é o inverso do processo de extrair o texto e as propriedades do documento e colocá-los no indexador. Confira também: índice, indexador, indexação.

**item**

Consulte a definição de: item shell.

**Classe de item**

Consulte a definição de: tipo de arquivo.

## <a name="k"></a>K

**Tipo**

Uma propriedade que fornece um Nome de tipo amigável e pode ser associada a uma lista de propriedades e um padrão de layout. O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo para o usuário final e foi definido como uma propriedade de cadeia de caracteres de vários valores (valores de cadeia de caracteres canônicas), portanto, você pode ter um valor kind "audio;video" ou "link;document". Alguns nomes de tipo amigáveis já estão associados a propriedades e padrões de layout. Por exemplo, itens associados a Kind.Picture e itens associados Kind.Document exibem propriedades diferentes mesmo quando estão na mesma exibição. Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout. Confira também: Associação de tipo, exibição de conteúdo, padrão de layout.

**Associação de tipo**

Uma propriedade no sistema de propriedades, chamada System.Kind, que determina quais modelos de UX são exibidos para um arquivo. Essa propriedade também fornece um nome amigável para o tipo do item e está vinculada à extensão de nome de arquivo. Confira também: Tipo.

## <a name="l"></a>L

**padrão de layout**

Uma das várias disposição para exibir propriedades. No Windows 7 e posterior, ao registrar um novo tipo de arquivo, você pode usar a exibição de conteúdo para registrar uma lista de propriedades personalizada e um padrão de layout para o tipo de arquivo. Você pode escolher entre quatro padrões de layout diferentes: Alfa (para resultados de pesquisa de documentos que contêm snippets de código), Beta (para resultados de pesquisa de email com snippets de código), Gama (semelhante a Alfa, mas com um layout de duas linhas em vez de quatro) e Delta (para mostrar muitas propriedades mais curtas, como com música e imagens). Confira também: exibição de conteúdo, Tipo, Associação de tipo.

## <a name="m"></a>M

**manipulador de metadados**

Às vezes, esse termo é usado para significar o manipulador de propriedades. Consulte definição para: manipulador de propriedades.

## <a name="n"></a>N

**extensão de namespace**

Consulte a definição de: Fonte de dados do Shell.

**passo a passo do namespace**

Um processo auxiliar que atravessa o namespace de um contêiner ou conjunto de contêineres, descobrindo cada item e possivelmente fazendo algo com cada um. A interface INamespaceWalk pode ser usada para usar qualquer parte do namespace Windows Explorer ou para descobrir os itens referenciados por um objeto de dados ou exibição. Verbos de contêiner (como "reproduzir" em contêineres de Artists) andam no namespace e descobrem os itens.

**consulta de idioma natural**

Consulte a definição de: NQS (Sintaxe de Consulta Natural).

**Sintaxe de consulta natural (NQS)**

Uma sintaxe de consulta mais descontraída do que o AQS e mais parecida com a linguagem humana. O NQS pode ser usado Windows Search para consultar o índice se o NQS estiver selecionado em vez do padrão, AQS. Consulte também: AQS (Advanced Query Syntax).

**palavra de ruído**

Uma palavra que é ignorada pelo Windows Search quando ela está presente nas restrições especificadas para a consulta de pesquisa, porque ela tem pouco valor discriminatório. Os exemplos incluem "and" e "the".

**NQS**

Consulte a definição de: NQS (Sintaxe de Consulta Natural).

## <a name="o"></a>O

**banco de dados de vinculação e incorporação de objeto (OLE DB)**

Um conjunto padrão de interfaces que fornece acesso heterogêneo a fontes diferentes de informações localizadas em qualquer lugar, como sistemas de arquivos, pastas de email e bancos de dados.

**OLE DB**

Consulte a definição de: banco de dados de vinculação e incorporação de objeto.

**OpenSearch descritor**

Um arquivo XML que descreve conexões de servidor disponíveis e formatos de resultado para uma fonte de dados específica baseada na Web. Esse arquivo contém um ou mais modelos de URL e usa uma extensão de nome de arquivo .osdx ao interagir com o shell Windows. Uma OpenSearch descrição é às vezes chamada de conector de pesquisa, embora seja apenas a parte de descrição de um conector. Confira também: pesquisar conector.

**OpenSearch padrão**

Uma coleção de formatos e protocolos simples usados para compartilhar resultados da pesquisa. Para obter mais informações, consulte o OpenSearch site ( https://github.com/dewitt/opensearch) .

## <a name="p"></a>P

**PerceivedType**

Uma ampla categoria de tipos de formato de arquivo. O PerceivedType foi introduzido no Windows XP e dá suporte a um conjunto limitado de tipos de arquivo conhecidos (exemplos incluem tipos de arquivo de imagem, texto, áudio e compactado). Tipos de arquivo, geralmente tipos de arquivo públicos, também podem ter um tipo percebido. Por exemplo, os tipos de arquivo de imagem .bmp, .png, .jpg e .gif também são do tipo percebido, imagem. Na camada de programação, PerceivedType é expresso como um inteiro. Como há código que usa Kind e PerceivedType, os proprietários de formato de arquivo devem registrar ambos. Por exemplo, "reproduzir tudo" depende de PerceivedType. Consulte também: tipo de arquivo.

**manipulador de visualização**

Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item shell a ser exibido no painel de visualização Windows Explorer.

**Previewer**

Às vezes, esse termo é usado para significar o manipulador de visualização. Consulte definição para: manipulador de visualização.

**manipulador de propriedades**

Um manipulador que converte dados armazenados em um arquivo em um esquema estruturado que é reconhecido por e pode ser acessado por Windows Explorer, Windows Search e outros aplicativos. Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para o arquivo. Os dados traduzidos incluem exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante. Cada manipulador de propriedades é associado a um tipo de arquivo específico, identificado pela extensão de nome de arquivo. Confira também: sistema de propriedades.

**manipulador de folha de propriedades**

Um manipulador usado para criar folhas de propriedades personalizadas com imagens e controles de interface do usuário que permitem a interação personalizada com um tipo de arquivo.

**sistema de propriedades**

Um sistema extensível de leitura/gravação de definições de dados que usa propriedades implementadas como pares nome-valor. Consulte também: manipulador de propriedades, item shell.

**valor da propriedade**

Um valor associado a um nome de propriedade para um item shell. Por exemplo, "Autor", "Tamanho" e "Data Tomada" são propriedades. Os valores de propriedade são expressos como uma estrutura PROPVARIANT.

**manipulador de protocolo**

Um manipulador que acessa fontes de conteúdo e fornece um objeto IUrlAccessor para um protocolo e uma URL especificados. Os manipuladores de protocolo Windows funcionalidade de Pesquisa e podem fornecer notificações de alteração para indexadores. Manipuladores de protocolo diferentes são necessários para indexar tipos específicos de armazenamentos de dados. Para fornecer uma experiência de usuário razoável, você também deve fornecer uma fonte de dados do Shell para o armazenamento de dados, além de implementar o manipulador de protocolo. O manipulador de protocolo expõe os itens no armazenamento de dados para o indexador, enquanto a fonte de dados do Shell expõe os itens no armazenamento de dados para o Shell.

## <a name="r"></a>R

**Restrição**

Uma condição que um arquivo deve atender para ser incluído nos resultados da pesquisa retornados pelo Windows Search.

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

um componente ou aplicativo que fornece dados para Windows pesquisa.

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

Uma única parte do conteúdo. Alguns itens de shell são fontes de conteúdo e outros não. Uma pasta é uma fonte de conteúdo, por exemplo, mas um arquivo de .jpg não é. Manipuladores de tipo de arquivo expõem itens de Shell. Em alguns contextos, "item" é usado para distinguir contêineres de não contidos. Consulte também: contêiner, fonte de conteúdo, manipulador de tipo de arquivo.

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

Uma cadeia de conexão baseada em URL que é usada para consultar um servidor Web para resultados da pesquisa. O modelo é semelhante a uma URL, mas contém vários valores de espaço reservado (como {searchTerms}) que o cliente deve substituir por dados sobre os resultados que deseja recuperar. a definição de modelos de URL é a chave para implementar os padrões de pesquisa e OpenSearch federada.

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

consulte a definição para: Windows serviço de pesquisa.

**Windows Pesquisar repositório de propriedades**

o cache dos valores de propriedade usados na implementação do serviço de pesquisa do Windows. esses valores de propriedade podem ser consultados programaticamente usando o provedor de OLE DB de pesquisa Windows. o repositório de propriedades de pesquisa Windows coleta e armazena as propriedades emitidas por manipuladores de filtro ou manipuladores de propriedade quando um item, como um documento do Word, é indexado. Esse armazenamento é Descartado e recriado quando o índice é recriado.

**Windows Serviço de pesquisa**

refere-se a Windows Search 3,0 e superior. Esse serviço analisa um conjunto de documentos, extrai informações úteis e, em seguida, organiza as informações extraídas para que as propriedades desses documentos possam ser retornadas de forma eficiente em resposta a consultas. Consulte também: catálogo.
