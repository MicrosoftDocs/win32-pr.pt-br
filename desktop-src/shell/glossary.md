---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
title: Glossário do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296728"
---
# <a name="shell-glossary"></a>Glossário do Shell

## <a name="a"></a>Um

<dl> <dt>

**associação**
</dt> <dd>

Um mapeamento de uma extensão de nome de arquivo (por exemplo,. mp3) ou protocolo (por exemplo, http) para um identificador programático (ProgID). Esse mapeamento é armazenado no registro como uma configuração por usuário com um fallback por computador. Os aplicativos que participam do sistema de programas padrão definem o mapeamento de associação para a extensão de nome de arquivo ou protocolo para apontarem para as chaves ProgID que eles possuem.

</dd> <dt>

**matriz de associação**
</dt> <dd>

Uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo. Por exemplo, um arquivo. jpg tem a seguinte matriz de associação em um sistema Windows padrão: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "a \\ \\ imagem de SystemFileAssociations de HKCR", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**bind**
</dt> <dd>

Para carregar ou associar código a dados. Por exemplo, um manipulador pode ser associado a uma fonte de dados do Shell.

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**nome canônico**
</dt> <dd>

O nome exclusivo de um recurso. Canônico significa "de acordo com as regras". Consulte também: nome do verbo canônico.

</dd> <dt>

**nome do verbo canônico**
</dt> <dd>

Um nome com neutralidade de idioma que pode ser usado programaticamente para se referir a um verbo, independentemente da cadeia de caracteres localizada na interface do usuário. Consulte também: nome canônico, verbo.

</dd> <dt>

**contêiner**
</dt> <dd>

Um tipo de item de shell que pode conter outros itens. Os itens em um contêiner são expostos ao namespace do shell usando uma fonte de dados do Shell. Os exemplos incluem pastas, unidades, servidores de rede e arquivos compactados com uma extensão de nome de arquivo. zip. Consulte também: fonte de dados do Shell, pasta, item de Shell.

</dd> <dt>

**content**
</dt> <dd>

Texto e propriedades associados a um item de shell ou a uma fonte de conteúdo que pode ser indexada.

</dd> <dt>

**fonte de conteúdo**
</dt> <dd>

Um item que pode ser acessado pelo indexador. As fontes de conteúdo são endereçáveis por uma URL e são fornecidas ao indexador por um manipulador de protocolo. Os exemplos incluem: arquivos e pastas do sistema de arquivos, itens e pastas do Microsoft Outlook, registros de banco de dados e itens armazenados do Microsoft SharePoint. Uma fonte de conteúdo pode ser exposta como itens de shell implementando uma fonte de dados do Shell. Consulte também: conteúdo, item de Shell.

</dd> <dt>

**content view (exibição de conteúdo)**
</dt> <dd>

Uma exibição no Windows Explorer (oferecida no Windows 7 e posterior) que exibe o conteúdo mais relevante para cada item da lista com base em sua associação de tipo ou extensão de nome de arquivo. A exibição de conteúdo usa uma lógica de redimensionamento que descarta Propriedades quando o tamanho da janela diminui para garantir que as propriedades mais críticas ainda tenham espaço para serem legíveis. Consulte também: padrão de layout, tipo, associação de tipo.

</dd> <dt>

**modo de exibição de conteúdo**
</dt> <dd>

Confira definição para: exibição de conteúdo.

</dd> <dt>

**menu de contexto**
</dt> <dd>

Esse termo às vezes é usado para significar o menu de atalho. Consulte definição para: menu de atalho.

</dd> <dt>

**manipulador de menu de contexto**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de menu de atalho. Consulte a definição de: manipulador de menu de atalho.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**manipulador de objeto de dados**
</dt> <dd>

Um manipulador que fornece formatos de área de transferência adicionais para o objeto de dados (IDataObject) de um item. Os objetos de dados são usados nos cenários de arrastar e soltar e copiar/colar.

</dd> <dt>

**fonte de dados**
</dt> <dd>

Esse termo às vezes é usado para significar o armazenamento de dados ou a fonte de dados do Shell. Consulte definição para: armazenamento de dados, fonte de dados do Shell.

</dd> <dt>

**armazenamento de dados**
</dt> <dd>

Um repositório de dados. Um armazenamento de dados pode ser exposto ao modelo de programação do shell como um contêiner usando uma fonte de dados do Shell. Os itens em um armazenamento de dados podem ser indexados pelo sistema de pesquisa do Windows usando um manipulador de protocolo.

</dd> <dt>

**composição de área de trabalho**
</dt> <dd>

Um recurso do Windows Vista que permite que janelas individuais sejam desenhadas para superfícies fora da tela na memória de vídeo em vez de serem desenhadas diretamente para o dispositivo de vídeo primário.

</dd> <dt>

**document**
</dt> <dd>

Um item de shell que contém texto e para o qual a interface IFilter poderia ser implementada.

</dd> <dt>

**descartar manipulador**
</dt> <dd>

Um manipulador que permite que um determinado tipo de item dê suporte a cenários de arrastar e soltar e copiar/colar.

</dd> <dt>

**soltar destino**
</dt> <dd>

Um objeto de dados que é arrastado e descartado em um arquivo. Consulte também: manipulador de dados, descartar manipulador.

</dd> <dt>

**verbo dinâmico**
</dt> <dd>

Um verbo que depende do estado de um item de shell ou do sistema; a aparência do item é baseada em estado e requer que o código de execução determine se o item deve aparecer. Consulte também: manipulador de menu de atalho, verbo estático, verbo.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Comando do Explorer**
</dt> <dd>

Um objeto que pode ser apresentado como um botão próximo à parte superior da janela do Windows Explorer que fornece funcionalidade para itens e contêineres nessa janela. Uma fonte de dados do Shell fornece os objetos de comando do Windows Explorer para um item de contêiner específico. Os comandos às vezes são usados como verbos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Associação de arquivo**
</dt> <dd>

Consulte a definição para: Associação de tipo de arquivo.

</dd> <dt>

**formato de arquivo**
</dt> <dd>

Um formato para dados armazenados em um arquivo que tem uma especificação de formato documentado. Os exemplos incluem o OLE DOCFILE, OPC, XML, ZIP e outras especificações de formato de arquivo conhecidas. Os criadores de tipo de arquivo geralmente usam um formato de arquivo existente como a base de um novo tipo de arquivo. Um formato de arquivo pode ser simplesmente uma definição que não é instanciada como um tipo de arquivo.

</dd> <dt>

**manipulador de formato de arquivo**
</dt> <dd>

Este termo é um sinônimo para o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

</dd> <dt>

**extensão de nome de arquivo**
</dt> <dd>

O indicador principal de um tipo de arquivo para itens do sistema de arquivos, é a parte do nome do arquivo que segue o ponto final. A extensão de nome de arquivo não pode conter espaços ou caracteres não ASCII e aplica-se somente a arquivos (não pastas). As extensões de nome de arquivo são comparadas usando uma função de comparação que não é sensível ao caso ou à localidade. Consulte também: formato de arquivo, tipo de arquivo.

</dd> <dt>

**tipo de arquivo**
</dt> <dd>

Um valor de extensão de nome de arquivo específico, como ". htm" ou ". jpg", que define uma classe de arquivos que são do mesmo tipo e têm um conjunto comum de associações. Consulte também: tipo, associação de tipo de arquivo.

</dd> <dt>

**associação de tipo de arquivo**
</dt> <dd>

Para uma extensão de nome de arquivo específica, os elementos da matriz de associação que definem onde os manipuladores e outros atributos podem ser registrados. Consulte também: matriz de associação, tipo de arquivo.

</dd> <dt>

**personalização de tipo de arquivo**
</dt> <dd>

Uma associação que habilita o Shell a personalizar como o Shell trata um tipo de arquivo. As personalizações de tipo de arquivo incluem: especificar o aplicativo usado para abrir o arquivo quando clicado duas vezes, adicionando comandos ao menu de atalho para um tipo de arquivo, especificando um ícone personalizado, especificando um tipo de conteúdo MIME para associar a um tipo de arquivo, especificando um tipo percebido e especificando um ou mais aplicativos associados por tipo de arquivo com a caixa de diálogo abrir com. Consulte também: Percebidotype.

</dd> <dt>

**manipulador de tipo de arquivo**
</dt> <dd>

Um manipulador registrado para um tipo de arquivo. Consulte também: manipulador.

</dd> <dt>

**pasta**
</dt> <dd>

Consulte a definição para: contêiner.

</dd> <dt>

**PIDL completo**
</dt> <dd>

Um PIDL que descreve exclusivamente um objeto relativo à pasta da área de trabalho.

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**cliques**
</dt> <dd>

Um objeto COM que fornece funcionalidade para um item de Shell. A maioria das fontes de dados de shell oferece um sistema extensível para ligar manipuladores a itens. Por exemplo, a pasta sistema de arquivos usa o sistema de associação para pesquisar os manipuladores de um determinado tipo de arquivo. Consulte também: Associação de arquivo, tipo de arquivo, personalização de tipo de arquivo.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**manipulador de ícone**
</dt> <dd>

Um manipulador que fornece as informações necessárias para gerar e armazenar em cache um ícone para um item. O armazenamento de dados do sistema de arquivos dá suporte ao carregamento de um manipulador de ícones para um item com base no tipo de arquivo, permitindo que esse manipulador forneça um ícone que é usado para todas as instâncias desse tipo de arquivo.

</dd> <dt>

**manipulador InfoTip**
</dt> <dd>

Um manipulador que fornece texto pop-up quando o usuário passa o ponteiro do mouse sobre um objeto da interface do usuário.

</dd> <dt>

**item**
</dt> <dd>

Consulte a definição de: item de Shell.

</dd> <dt>

**classe de item**
</dt> <dd>

Consulte definição para: tipo de arquivo.

</dd> <dt>

**lista de identificadores de item**
</dt> <dd>

Sequência de uma ou mais estruturas SHITEMID que define exclusivamente um objeto em relação a algum objeto raiz.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Tipo**
</dt> <dd>

Uma propriedade que fornece um nome de tipo amigável e pode ser associada a uma lista de propriedades e um padrão de layout. O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo para o usuário final e foi definido como uma propriedade de cadeia de caracteres com vários valores (valores de cadeia de caracteres canônicos), assim, você pode ter um valor de tipo de "áudio; vídeo" ou "vincular; documento". Alguns nomes de tipos amigáveis do usuário já estão associados a propriedades e padrões de layout. Por exemplo, itens associados ao tipo. imagem e itens associados a Kind.Document exibem propriedades diferentes mesmo quando estão na mesma exibição. Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout. Consulte também: espécie de associação, exibição de conteúdo, padrão de layout.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**padrão de layout**
</dt> <dd>

Uma das várias disposições para exibir propriedades. No Windows 7 e posterior, ao registrar um novo tipo de arquivo, você pode usar a exibição de conteúdo para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo. Você pode escolher entre quatro padrões de layout diferentes: alfa (para resultados de pesquisa de documentos que contêm trechos de código), beta (para resultados de pesquisa de email com trechos de código), gama (semelhante a alfa, mas com um layout de duas linhas em vez de quatro) e Delta (para mostrar muitas propriedades mais curtas, como com música e imagens). Consulte também: exibição de conteúdo, tipo, associação de tipo.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**manipulador de metadados**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de propriedades. Consulte a definição de: manipulador de propriedade.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**extensão do namespace**
</dt> <dd>

Consulte a definição de: fonte de dados do Shell.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Banco de dados de vinculação e incorporação de objetos (OLE DB)**
</dt> <dd>

Um conjunto padrão de interfaces que fornece acesso heterogêneo a fontes diferentes de informações localizadas em qualquer lugar, como sistemas de arquivos, pastas de email e bancos de dados.

</dd> <dt>

**OLE DB**
</dt> <dd>

Consulte definição para: vinculação de objetos e banco de dados de incorporação.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**PerceivedType**
</dt> <dd>

Uma categoria ampla de tipos de formato de arquivo. O percebidatype foi introduzido no Windows XP e dá suporte a um conjunto limitado de tipos de arquivo conhecidos (exemplos incluem imagem, texto, áudio e tipos de arquivo compactados). Tipos de arquivo, geralmente tipos de arquivo públicos, também podem ter um tipo percebido. Por exemplo, o arquivo de imagem Types. bmp,. png,. jpg e. gif também são do tipo percebido, Image. Na camada de programação, Percebidotype é expresso como um inteiro. Como há código que usa tipo e Percebidotype, os proprietários de formato de arquivo devem registrar ambos. Por exemplo, "reproduzir tudo" depende de Percebidotype. Consulte também: tipo de arquivo.

</dd> <dt>

**Gerenciador de visualização**
</dt> <dd>

Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item de Shell a ser exibido no painel de visualização do Windows Explorer.

</dd> <dt>

**manipulador de propriedades**
</dt> <dd>

Um manipulador que traduz dados armazenados em um arquivo em um esquema estruturado que é reconhecido pelo e pode ser acessado pelo Windows Explorer, pelo Windows Search e por outros aplicativos. Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para o arquivo. Os dados traduzidos incluem exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante. Cada manipulador de propriedade é associado a um tipo de arquivo específico, identificado pela extensão de nome de arquivo. Consulte também: sistema de propriedades.

</dd> <dt>

**manipulador de folhas de propriedades**
</dt> <dd>

Um manipulador que é usado para criar folhas de propriedades personalizadas com imagens e controles da interface do usuário que permitem a interação personalizada com um tipo de arquivo.

</dd> <dt>

**sistema de propriedades**
</dt> <dd>

Um sistema de leitura/gravação extensível de definições de dados que usa propriedades implementadas como pares de nome-valor. Consulte também: manipulador de propriedades, item de Shell.

</dd> <dt>

**valor da propriedade**
</dt> <dd>

Um valor associado a um nome de propriedade para um item de Shell. Por exemplo, "autor", "tamanho" e "data de uso" são propriedades. Os valores de propriedade são expressos como uma estrutura PROPVARIANT.

</dd> <dt>

**manipulador de protocolo**
</dt> <dd>

Um manipulador que acessa fontes de conteúdo e fornece um objeto IUrlAccessor para um protocolo e uma URL especificados. Os manipuladores de protocolo estendem a funcionalidade de pesquisa do Windows e podem fornecer notificações de alteração aos indexadores. Manipuladores de protocolo diferentes são necessários para indexar tipos específicos de armazenamentos de dados. Para fornecer uma experiência de usuário razoável, você também deve fornecer uma fonte de dados do Shell para o armazenamento de dados, além de implementar seu manipulador de protocolo. O manipulador de protocolo expõe os itens no armazenamento de dados para o indexador, enquanto a fonte de dados do Shell expõe os itens no armazenamento de dados para o Shell.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**PIDL relativo**
</dt> <dd>

Um PIDL que é relativo a algum objeto raiz no namespace do shell que não seja a pasta da área de trabalho. Normalmente, essa é a pasta pai do item.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Fonte de dados do Shell**
</dt> <dd>

Um componente que é usado para estender o namespace do Shell e expor itens em um armazenamento de dados. No passado, a fonte de dados do Shell era chamada de extensão de namespace do Shell. Consulte também: contêiner, manipulador, item de Shell.

</dd> <dt>

**Extensão do shell**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

</dd> <dt>

**Manipulador de extensão de Shell**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

</dd> <dt>

**Manipulador de Shell**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de tipo de arquivo. Consulte a definição para: manipulador de tipo de arquivo.

</dd> <dt>

**Item do Shell**
</dt> <dd>

Uma única parte do conteúdo. Alguns itens de shell são fontes de conteúdo e outros não. Uma pasta é uma fonte de conteúdo, por exemplo, mas um arquivo. jpg não é. Manipuladores de tipo de arquivo expõem itens de Shell. Em alguns contextos, "item" é usado para distinguir contêineres de não contidos. Consulte também: contêiner, fonte de conteúdo, manipulador de tipo de arquivo.

</dd> <dt>

**Extensão do namespace do Shell**
</dt> <dd>

Esse termo às vezes é usado para significar a fonte de dados do Shell. Consulte a definição de: fonte de dados do Shell.

</dd> <dt>

**menu de atalho**
</dt> <dd>

Uma interface do usuário que é usada para apresentar uma coleção de verbos associados a um elemento de interface do usuário, como um arquivo ou uma pasta.

</dd> <dt>

**Manipulador de menu de atalho**
</dt> <dd>

Um manipulador que adiciona verbos para um item ou itens. Esses verbos são normalmente exibidos em um menu de atalho. Consulte também: menu de atalho.

</dd> <dt>

**PIDL simples**
</dt> <dd>

Um PIDL que é analisado sem verificação de disco.

</dd> <dt>

**verbo estático**
</dt> <dd>

Um verbo que se aplica a um item de shell sem a necessidade de inspecionar o estado atual de um item ou sistema. Um verbo estático é baseado em um registro estático dos elementos associados de um item e não é alterado.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**manipulador de miniaturas**
</dt> <dd>

Um manipulador que fornece uma imagem estática para representar um item de Shell.

</dd> <dt>

**provedor de miniatura**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de miniaturas. Consulte a definição de: manipulador de miniatura.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**nome de tipo amigável do usuário**
</dt> <dd>

Consulte a definição de: Kind.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**verbo**
</dt> <dd>

Uma ação individual que pode ser chamada por um item de Shell. Os exemplos incluem abrir e imprimir. Os verbos são, às vezes, chamados de comandos ou tarefas. Consulte também: verbo dinâmico, manipulador de menu de atalho, verbo estático.

</dd> <dt>

**manipulador de verbo**
</dt> <dd>

Esse termo às vezes é usado para significar o manipulador de menu de atalho. Consulte a definição de: manipulador de menu de atalho.

</dd> </dl>

 

 



