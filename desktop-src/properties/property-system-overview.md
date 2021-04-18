---
description: O sistema de propriedades do Windows é um sistema de leitura/gravação extensível de definições de dados que fornece uma maneira uniforme de expressar os metadados sobre itens de Shell.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Visão geral do sistema de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab3a17eacdbaa9a5d0255004ba544b7c3f7ff2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785103"
---
# <a name="property-system-overview"></a>Visão geral do sistema de propriedades

O sistema de propriedades do Windows é um sistema de leitura/gravação extensível de definições de dados que fornece uma maneira uniforme de expressar os metadados sobre itens de Shell. O sistema de propriedades do Windows no Windows Vista e posterior permite que você armazene e recupere metadados para itens de Shell. Um item de Shell é qualquer conteúdo único, como um arquivo, uma pasta, um email ou um contato. Uma propriedade é uma parte individual dos metadados associados a um item de Shell. Os valores de propriedade são expressos como uma estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Este tópico é organizado da seguinte maneira:

-   [Introdução](#introduction)
-   [Cenários de desenvolvimento](#development-scenarios)
-   [Propriedades e pesquisa do Windows](#properties-and-windows-search)
-   [Observação para implementadores](#note-to-implementers)
-   [Documentação do sistema de propriedades do Windows](#windows-property-system-documentation)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

As propriedades são identificadas exclusivamente por seu nome canônico (como `System.Document.LastAuthor` ) e chave de propriedade (como `PKEY_Document_LastAuthor` ). Uma chave de propriedade (PKEY) é a parte do nome de um par de nome-valor que consiste em um PKEY/PROPVARIANT ou uma cadeia de caracteres/PROPVARIANT, em que a cadeia de caracteres é o nome canônico do PKEY (como `System.Document.LastAuthor` ). Um PKEY é uma definição que diz ao sistema de propriedades tudo o que ele precisa saber sobre a propriedade, enquanto o valor é uma instância real da propriedade. Um PKEY internamente contém um FormatID e propID.

Uma propriedade individual consiste nas seguintes três partes:

-   Um nome canônico, como `System.Music.Artist` .
-   Uma descrição do esquema, que é especificada no formato de arquivo XML. propDesc e expressa programaticamente por meio de [**IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Um valor, como o nome de um cantor.

A descrição do esquema consiste em informações sobre a propriedade, como o nome da propriedade, o tipo de dados, as restrições, informações sobre como a propriedade interage com exibições e o sistema de pesquisa e assim por diante. O nome e a descrição do esquema são definidos globalmente e são os mesmos para todos os itens e tipos. Um valor é específico de um item individual. Ou seja, a `System.Music.Artist` propriedade é sempre definida como uma cadeia de caracteres de valores múltiplos, mas pode ter um valor diferente (ou nenhum valor) para cada item.

Um manipulador de propriedades traduz os dados armazenados em um arquivo em um esquema estruturado que é reconhecido pelo e pode ser acessado pelo Windows Explorer, pelo Windows Search e por outros aplicativos. Esses sistemas podem interagir com o manipulador de propriedades para gravar e ler propriedades de e para o arquivo. Os dados traduzidos são expostos programaticamente e mostrados para o usuário por meio do Windows Explorer em uma variedade de contextos, incluindo exibição de detalhes, infotips, painel de detalhes, páginas de propriedades e assim por diante. Cada manipulador de propriedade é associado a um tipo de arquivo específico, que é identificado pela extensão de nome de arquivo. Os desenvolvedores devem implementar um manipulador de propriedades que produza e consuma o formato nativo do tipo de arquivo, como. jpg ou. png, ou usar o armazenamento de propriedades In-Memory, que produz e consome o formato binário MS-PROPSTORE.

O sistema de propriedades do Windows cria um modelo de dados abstrato que fornece um nível de abstração de formatos de arquivo individuais. O modelo de dados abstrato fornecido pelo sistema de propriedades do Windows é um método para ler e gravar um conjunto extensível de valores nomeados associados a um item de Shell. A expressão de valor é flexível, dá suporte a muitos tipos de dados e é extensível, habilitando dados arbitrários (**\_ blob VT**) e objetos a serem expressos como um valor.

Devido à abstração, você pode consultar os atributos ou os metadados de qualquer item. Exemplos de itens que podem ser dissociados incluem documentos Microsoft Office, marcas ID3 e o AutoCAD e outros softwares proprietários de terceiros. Da mesma forma, se você tiver um arquivo. jpeg, poderá usar os codecs. jpeg e EXIF para ler os bytes do arquivo para descobrir quais são as dimensões da imagem. Se você tiver um arquivo. png, você precisará de um codec diferente e um código diferente para fazer isso. O uso do sistema de propriedades do Windows evita esse tipo de problema. Se você implementar um novo tipo de arquivo, terá a opção de conectar-se à abstração uniforme oferecida pelo sistema de propriedades do Windows e especificar como tornar seus metadados consumíveis. Por esses motivos, é sempre preferível usar a plataforma comum fornecida pelo sistema de propriedades do Windows.

## <a name="development-scenarios"></a>Cenários de desenvolvimento

As propriedades são expressas por produtores e consumidores. Nesse contexto, os produtores são os inventores das propriedades no sistema de propriedades do Windows e os consumidores são aplicativos (e seus desenvolvedores) que consomem informações de propriedade deste sistema. Os usos do e dos participantes no sistema de propriedades do Windows são identificados na tabela a seguir.



| Uso do sistema de propriedades do Windows                                                                                                                                                                                            | Participante |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Um bloco de construção que fornece um registro extensível de descrições de propriedade, uma implementação de armazenamento de propriedade na memória e serviços para associação a manipuladores de propriedade, conversão de tipos e serialização de armazenamentos de propriedade. | Consumidor    |
| Aplicativos que desejam ler e gravar propriedades de forma abstrata.                                                                                                                                                       | Consumidor    |
| Inventores de propriedade que definem novas propriedades para o sistema de propriedades definindo esquemas de propriedade personalizada e desenvolvendo seus próprios manipuladores de propriedade.                                                                          | Produtor    |
| Proprietários de formato de arquivo que desejam habilitar o acesso às propriedades armazenadas em seus formatos de arquivo personalizados.                                                                                                                           | Produtor    |



 

Os consumidores consomem Propriedades, esquemas e manipuladores de propriedade existentes. As propriedades disponíveis para consumo incluem propriedades de leitura/gravação de manipuladores de propriedade para tipos de arquivo com suporte e também podem incluir algumas propriedades personalizadas. Os esquemas disponíveis incluem pelo menos o esquema do sistema e, às vezes, outros também. Um consumidor pode criar um aplicativo para consumir metadados e criar uma exibição com base no artista, independentemente de quais pastas os itens estão armazenados. A hierarquia de pastas de arquivos é irrelevante. Por exemplo, você pode especificar todos os itens de música por um determinado cantor sem se preocupar com a localização desses itens. Esse cenário complexo de ponta a ponta não se limita ao sistema de propriedades do Windows, mas envolve vários componentes diferentes, como as pastas de indexação e pesquisa.

Os inventores de propriedade ou desenvolvedores de terceiros são produtores no sistema de propriedades do Windows. Ao se preparar para definir uma nova propriedade, primeiro Inspecione o conjunto de propriedades que o Windows define. Se você encontrar um que atenda às suas necessidades, do tipo e da semântica que correspondem ao seu uso necessário, use essa propriedade e não crie uma nova. Se você estiver definindo uma nova propriedade personalizada, tente obter o contrato com outros desenvolvedores que talvez queiram usá-lo e publicar o resultado desse contrato para que eles possam ingressar na Comunidade de usuários dessa propriedade.

Os produtores podem aproveitar a funcionalidade do Windows Explorer. Por exemplo, se você estiver escrevendo um novo formato de imagem e implementar um manipulador de propriedades, o novo formato de arquivo ficará disponível no Windows Explorer. Os usuários podem marcar suas fotografias e dinamizar sua coleção de fotografias com base em qualquer propriedade no sistema de propriedades do Windows. Na verdade, tudo o que o Shell faz com propriedades, desenvolvedores de terceiros podem fazer em seus próprios aplicativos. Isso inclui agrupamento, classificação, consulta e exibição de propriedades completas. A experiência do usuário que o Windows Explorer fornece pode ser amplamente implementada por terceiros com APIs disponíveis publicamente. O Windows Explorer pode ser substituído ou estendido usando essas APIs.

Do ponto de vista de um aplicativo que usa o modelo de dados do Shell, há uma grande variedade de cenários que envolvem o uso do sistema de propriedades do Windows. Os aplicativos de gerenciamento de mídia são um exemplo proeminente. Os principais cenários do sistema de propriedades incluem cenários como a leitura da Propriedade Keyword de uma fotografia ou a definição da propriedade DateTaken. Exemplos de cenários de integração de ponta a ponta que o sistema de propriedades do Windows habilita, mas que exigem que vários outros componentes funcionem, incluindo a exibição de todas as imagens ou a localização de um documento que contém uma palavra-chave.

## <a name="properties-and-windows-search"></a>Propriedades e pesquisa do Windows

As propriedades servem para produtores e consumidores quando eles fazem interface com o Windows Search e indexação. O Windows Search tem um cache de valores de propriedade que são usados na implementação do Windows Serviço de Pesquisa (WSS). Esses valores de propriedade podem ser consultados programaticamente usando o provedor de OLE DB do Windows Search ou por meio de [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), que representa os itens nos resultados da pesquisa e exibições baseadas em consulta. Em seguida, o Windows Search coleta e armazena as propriedades emitidas por manipuladores de filtro ou manipuladores de propriedades quando um item, como um documento do Word, é indexado. Esse armazenamento é Descartado e recriado quando o índice é recriado.

> [!Note]  
> Lembre-se de que quando você registra novamente um esquema, as alterações feitas em atributos de propriedades definidas anteriormente podem não ser respeitadas pelo indexador. A solução é recriar o índice ou introduzir novas propriedades que reflitam as alterações em vez de atualizar as antigas (não recomendado). Para obter mais informações, consulte [Observação para implementadores](#note-to-implementers) mais adiante neste tópico.

 

Por exemplo, um desenvolvedor que cria um aplicativo de mídia deseja mostrar aos usuários do aplicativo todas as músicas disponíveis por um determinado artista. O aplicativo forneceria ao usuário uma lista de artistas disponíveis e, em seguida, geraria uma lista de todas as músicas disponíveis pelo artista que o usuário selecionar. Ou um usuário final pode querer fazer uma consulta para? artista: Sinfonia? e ser exposto à lista completa de propriedades disponíveis no decorrer de sua pesquisa. Este exemplo envolve o uso do namespace do Shell, manipuladores de propriedade e/ou consulta do índice por meio de um dos seguintes:

-   Uma fonte de dados do Shell.
-   Um provedor OLE DB.
-   Um arquivo de pesquisa salvo (. Search-MS) que é usado para iniciar uma consulta navegando até o arquivo de pesquisa no Windows Explorer ou ligando para [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de forma programática.

> [!Note]  
> Embora a `System.Kind` propriedade não participe desse cenário de aplicativo de mídia, ela pode ser usada para criar uma consulta que retornaria todos os arquivos. Search-MS em um escopo específico.

 

A maneira preferida de acessar as APIs de pesquisa e criar aplicativos de pesquisa do Windows é por meio de uma fonte de dados do Shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) é um componente que pode criar instâncias da fonte de dados da pasta de pesquisa, que é um tipo de fonte de dados "virtual" fornecida pelo shell que pode executar consultas em outras fontes de dados no namespace do Shell e enumerar os resultados. Isso pode ser feito usando o indexador ou enumerando manualmente e inspecionando itens nos escopos especificados.

Desenvolvedores de terceiros podem criar aplicativos que consomem os dados no índice por meio de consultas programáticas e podem estender os dados no índice para tipos de arquivo e item personalizados a serem indexados pelo Windows Search. Se você quiser mostrar os resultados da consulta no Windows Explorer, deverá implementar uma fonte de dados do Shell antes de poder criar um manipulador de protocolo para estender o índice. No entanto, se todas as consultas forem programáticas (por meio de OLE DB, por exemplo) e interpretadas pelo código do aplicativo? s, em vez do Shell, um namespace do Shell ainda é preferido, mas não é necessário. Um manipulador de protocolo é necessário para que o Windows Obtenha informações sobre o conteúdo do arquivo, como itens em bancos de dados ou tipos de arquivo personalizados. Embora o Windows Search possa indexar o nome e as propriedades do arquivo, o Windows não tem informações sobre o conteúdo do arquivo. Como resultado, esses itens não podem ser indexados ou expostos no Shell do Windows. Ao implementar um manipulador de protocolo personalizado, você pode expor esses itens. Para obter uma lista de manipuladores identificados pelo cenário de desenvolvedor que você está tentando obter, consulte "visão geral de manipuladores" no [Windows Search como uma plataforma de desenvolvimento](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Algumas vezes, uma fonte de dados do Shell é conhecida como extensão de namespace do Shell. Um manipulador é, às vezes, conhecido como uma extensão de shell ou um manipulador de extensão de Shell.

 

## <a name="note-to-implementers"></a>Observação para implementadores

Devido a possíveis dificuldades que o indexador pode ter ao consumir o esquema do sistema de propriedades, é fundamental que você defina atributos com cuidado e estrategicamente para a primeira versão do esquema. Qualquer alteração nos atributos (tipo, largura da coluna, se indexible) não será refletida no banco de dados depois que um esquema tiver sido registrado. As únicas maneiras de ter essas alterações reconhecidas depois que o esquema foi registrado uma vez em um sistema seriam recriar o índice e, em seguida, registrar o novo esquema, ou registrar o esquema e, em seguida, criar uma nova propriedade para cada versão subsequente; por exemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , e assim por diante. Não recomendamos a criação de novas propriedades dessa maneira, pois várias colunas estranhas podem afetar o desempenho do sistema.

## <a name="windows-property-system-documentation"></a>Documentação do sistema de propriedades do Windows

O restante desta documentação contém as seguintes seções:

-   [Guia do desenvolvedor do sistema de propriedades do Windows](property-system-developer-s-guide.md)

    Descreve detalhadamente como implementar os principais cenários de desenvolvimento usando o sistema de propriedades do Windows.

-   [Referência do sistema de propriedades](property-system-reference.md)

    Documenta as [Propriedades do Windows](props.md), o [esquema de descrição de propriedade](property-description-schema.md), as [interfaces](interfaces.md), as [funções](functions.md), as [estruturas](structures.md)e as [constantes, enumerações e sinalizadores](constants--enumerations--and-flags.md) do sistema de propriedades do Windows.

-   [Exemplos de código do sistema de propriedades](property-system-code-samples.md)

    Descreve exemplos que demonstram como usar o sistema de propriedades do Windows.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter informações sobre como reutilizar o repositório de propriedades In-Memory, consulte [inicializando manipuladores de propriedade](building-property-handlers-property-handlers.md) e [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Para obter uma especificação do formato de arquivo binário do armazenamento de propriedades da Microsoft, consulte [ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   A relação entre a pesquisa e a indexação do Windows e como estender o índice é explicada nos seguintes tópicos do Windows Search:
    -   [Desenvolvendo manipuladores de filtro para o Windows Search](../search/-search-ifilter-conceptual.md)
    -   [Desenvolvendo manipuladores de protocolo para o Windows Search](../search/-search-3x-wds-phaddins.md)
    -   [Desenvolvendo manipuladores de propriedade para o Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Para obter o download do SDK do Windows Vista ou atualizado, consulte a [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia do desenvolvedor do sistema de propriedades do Windows](property-system-developer-s-guide.md)
</dt> <dt>

[Referência do sistema de propriedades](property-system-reference.md)
</dt> <dt>

[Exemplos de código do sistema de propriedades](property-system-code-samples.md)
</dt> </dl>

 

 
