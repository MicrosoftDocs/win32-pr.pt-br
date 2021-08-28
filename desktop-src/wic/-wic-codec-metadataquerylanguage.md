---
description: este tópico apresenta a linguagem de consulta de metadados para o componente de Windows Imaging (WIC).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Visão geral da linguagem de consulta de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e141c543cae90ff99d8c0509a0f5802dba1139
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885214"
---
# <a name="metadata-query-language-overview"></a>Visão geral da linguagem de consulta de metadados

este tópico apresenta a linguagem de consulta de metadados para o componente de Windows Imaging (WIC). Você usa a linguagem de consulta de metadados para criar expressões que localizam dados específicos (itens de metadados) e locais (blocos de metadados) dentro dos metadados de uma imagem.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Introdução](#introduction)
-   [Anatomia de uma expressão de caminho](#anatomy-of-a-path-expression)
    -   [Bloquear Seleção](#block-selection)
    -   [Seleção de item](#item-selection)
    -   [Caractere de escape](#escape-character)
    -   [Exemplos de expressões](#sample-expressions)
-   [Expressões de política de metadados de foto](#photo-metadata-policy-expressions)
-   [Resumo da linguagem de consulta de metadados](#metadata-query-language-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com o sistema de metadados do WIC, conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md) e no acesso aos metadados, conforme descrito na [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).

## <a name="introduction"></a>Introdução

Você interage com a plataforma de metadados principalmente por meio de dois componentes de Component Object Model (COM): um leitor de consulta, representado pela interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , e um gravador de consulta, representado pela interface [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Esses componentes permitem que você leia ou grave metadados usando a linguagem de consulta de metadados. A linguagem de consulta descreve a sintaxe de uma expressão de caminho e os componentes de consulta usam essa expressão de caminho para acessar os metadados desejados. Esta expressão de caminho descreve o local de um item ou bloco de metadados.

Um bloco de metadados é um grupo nomeado de metadados em um formato específico. Um bloco de metadados pode conter itens de metadados individuais, como um autor ou tempo de criação e blocos de metadados adicionais. O nome de um bloco de metadados é determinado por seu formato. Por exemplo, um bloco de metadados contendo metadados App1 seria nomeado "app1". Os formatos de metadados comuns incluem App1, EXIF, IFD e XMP.

Um item de metadados é um par de nome/valor que descreve características como autor, título e classificação.

Uma expressão de caminho contém um ou mais nomes de blocos de metadados. Ele também pode especificar um item de metadados dentro de um bloco de metadados. A expressão de caminho a seguir representa um bloco App1 que contém um bloco IFD que contém o item de metadados:

-   /App1/IFD/{UShort = 18249}

O diagrama a seguir ilustra a composição de um exemplo de imagem JPEG com quatro blocos de metadados raiz: App0, App1, XMP e um bloco desconhecido. Cada item realçado anota o tipo de metadados (bloco ou item) e a expressão de consulta usada para recuperar os dados.

![imagem JPEG com texto explicativo de metadados](graphics/jpegwithcallouts.png)

> [!Note]  
> O conteúdo deste diagrama é referenciado em todo este documento e é usado em muitos dos exemplos.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomia de uma expressão de caminho

Para acessar metadados usando as APIs do WIC, uma expressão de consulta totalmente qualificada deve ser usada na maioria dos casos. Este tópico discute expressões totalmente qualificadas para acessar metadados. Se você precisar de informações sobre os casos em que as expressões não totalmente qualificadas são usadas, consulte a seção expressão de política de metadados de foto mais adiante neste documento.

O que é uma expressão de consulta totalmente qualificada? No WIC, uma expressão totalmente qualificada é uma cadeia de caracteres que começa com a barra de caracteres de caminho (/), seguida por um caminho de navegação para um bloco de metadados ou um item de metadados específico. Cada etapa dentro do caminho de navegação é separada por uma barra, formando uma expressão para acessar um bloco de metadados ou um item de metadados. Por exemplo, a seguir está uma expressão de consulta totalmente qualificada que acessa a classificação de fotos da Microsoft em um bloco IFD que está aninhado em um bloco APP1:

-   /App1/IFD/{UShort = 18249}

Quando o WIC analisa essa expressão, ele primeiro procura o bloco de metadados App1 nos metadados da imagem. Se o bloco App1 for encontrado, ele continuará sua pesquisa procurando o bloco de metadados IFD aninhado. Se o bloco IFD for encontrado, ele procurará o item de metadados específico, nesse caso, a classificação MicrosoftPhoto sob a marca 18249, dentro do bloco de metadados IFD. Se, a qualquer momento, o WIC não encontrar um bloco ou item de metadados, ele anulará a consulta.

### <a name="block-selection"></a>Bloquear seleção

A expressão de consulta de metadados do WIC mais simples é uma expressão para obter um leitor de consulta/gravador para um bloco de metadados específico. A obtenção de um leitor/gravador de consulta permite direcionar consultas subsequentes diretamente a um bloco de metadados aninhado sem lidar com seu bloco pai. Uma expressão de consulta de seleção de bloco é um caminho de navegação para o bloco de metadados desejado. Por exemplo, na ilustração anterior, há cinco blocos de metadados, dois dos quais estão aninhados em outros blocos de metadados. A seguir estão as expressões de caminho para cada bloco de metadados no exemplo de JPEG:

-   /app0
-   /App1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Quando você usa um leitor de consulta/gravador para executar uma consulta, ele retorna um novo leitor/gravador de consulta que realiza consultas de serviços dentro do escopo do bloco de metadados especificado. Por exemplo, se você executar a consulta "/app1", um novo leitor de consulta será obtido e as consultas ao novo leitor serão relativas ao bloco App1. Isso significa que a consulta "/IFD" é válida para o novo leitor porque o bloco App1 contém um bloco IFD. No entanto, "/XMP" não funcionaria porque este bloco App1 não contém um bloco de metadados XMP.

A linguagem de consulta também dá suporte a uma notação de índice. A notação de índice fornece acesso a um bloco de metadados específico quando há vários blocos do mesmo tipo. Para o exemplo de JPEG, a seguinte expressão de caminho indexado pode ser usada:

-   /\[\]IFD 0 App1 \[ / \] 0

Na linguagem de consulta, todos os índices começam em zero. Na expressão anterior, as primeiras zero consultas para o primeiro bloco App1 e o segundo zero consultam o primeiro bloco de IFD aninhado. A notação de índice ainda pode ser usada mesmo quando vários blocos do mesmo tipo não existem. Se o exemplo JPEG incluísse um segundo bloco App1 com um bloco de IFD inserido, a expressão "/ \[ 1 \] App1/IFD" seria usada para acessar o segundo bloco App1.

A notação de índice se torna mais comum ao lidar com partes de texto PNG, pois é provável que a imagem PNG tenha mais de uma parte de texto.

> [!Note]  
> Não há suporte para índices de matriz multidimensional.

 

### <a name="item-selection"></a>Seleção de item

Você pode acessar os itens de metadados em um bloco de metadados criando as expressões de seleção de bloco. Considere as propriedades XMP e classificação de fotos da Microsoft no exemplo JPEG. Esses metadados existem em dois blocos de metadados: os blocos App1/IFD e XMP. Portanto, mais de uma expressão pode ser usada para acessar os mesmos dados. A expressão a seguir acessa a classificação MicrosoftPhoto no bloco XMP:

-   /XMP/XMP: classificação

A parte "XMP:" da expressão é um identificador amigável de esquema. O XMP é um padrão extensível e permite que entidades de terceiros publiquem seus próprios esquemas que definem como armazenar determinados itens de metadados. Um esquema XMP é totalmente identificado por uma URL, mas o WIC fornece um conjunto de identificadores amigáveis para esquemas bem conhecidos. Para obter mais informações, consulte o tópico de [consultas de metadados do formato de imagem nativa](-wic-native-image-format-metadata-queries.md) .

Para imagens JPEG, as informações de classificação também podem ser armazenadas no bloco de IFD aninhado App1. No entanto, diferentemente do exemplo de classificação XMP, o bloco IFD não usa um nome de esquema para acessar as informações de classificação. Em vez disso, use uma expressão de dados. A expressão a seguir é usada para acessar a classificação MicrosoftPhoto no bloco de IFD aninhado do APP1:

-   /App1/IFD/{UShort = 18249}

Nessa expressão, a parte "/app1/IFD" da expressão é o caminho de navegação para o bloco IFD (conforme discutido anteriormente na seção seleção de bloco). A segunda parte da expressão "/{UShort = 18249}" acessa os dados. Essa parte da expressão instrui o analisador de consulta a localizar os dados inseridos na marca curta sem sinal que tem o identificador de marca 18249.

> [!Note]  
> Para obter uma lista de formatos de metadados comuns com suporte em cada formato de imagem em, consulte o tópico de [consultas de metadados de formato de imagem nativa](-wic-native-image-format-metadata-queries.md) .

 

{Ushort = 18249} é uma expressão de dados e pode receber várias formas. Uma expressão de dados é uma expressão de duas partes que contém a marca ou a chave de metadados solicitada, neste caso, "18249", e o tipo de dados da chave, neste caso, "UShort". As duas partes são separadas por um sinal de igual (=). WICsupports a maioria dos tipos de dados comuns de C/C++. Os seguintes tipos de dados são aceitos pela linguagem de consulta:

-   char
-   uchar
-   short
-   ushort
-   long
-   ulong
-   INT
-   uint
-   longlong
-   FLOAT
-   double
-   str
-   wstr
-   guid
-   bool

> [!Note]  
> Essa lista especifica apenas os tipos de dados com suporte pela linguagem de consulta de metadados. Use esses tipos de dados ao criar uma expressão de dados de consulta de metadados, como {UShort = 18249}. O WIC retorna o valor do item de metadados na forma de PROPVARIANT, que define seu próprio sistema de tipos.

 

O "18249" no exemplo é a marca de dados. Esse número específico é definido pela Microsoft para conter a classificação MicrosoftPhoto. A marca de dados pode ser qualquer número, Cadeia de caracteres ou GUID, dependendo do item de dados que você está procurando

Ao contrário do exemplo de classificação XMP, não há nenhuma colisão de nome para o valor de classificação no bloco App1/IFD. Isso ocorre porque o valor de classificação XMP é realmente armazenado em uma marca UShort diferente, 18246. Assim, a expressão para acessar a classificação XMP no bloco App1/IFD é:

-   /App1/IFD/{UShort = 18246}

> [!Note]  
> Para obter uma descrição formal da linguagem de consulta de metadados, consulte a seção de resumo da linguagem de consulta de metadados mais adiante neste documento.

 

### <a name="escape-character"></a>Caractere de escape

A linguagem de consulta não diferencia maiúsculas de minúsculas e trata todos os caracteres em minúsculas. No entanto, alguns formatos de metadados (como XMP) diferenciam maiúsculas de minúsculas. Ao trabalhar com um formato de metadados que diferencia maiúsculas de minúsculas, use o caractere de barra invertida ( \\ ) quando desejar especificar um caractere maiúsculo.

O caractere de escape é consumido pelo analisador de idioma e o seguinte caractere que o segue é interpretado diretamente. Por exemplo, a expressão {Char = \\ \\ } é resolvida como ' \\ ' e {Char = \\ C} é resolvido como um C em maiúsculas. Sem o caractere de escape, {Char = \\ } seria uma expressão inválida e {Char = C} seria interpretado como um C em minúsculas. Certifique-se de usar o caractere de escape de barra invertida antes de todas as letras maiúsculas nos formatos de metadados diferenciarem maiúsculas de minúsculas.

### <a name="sample-expressions"></a>Exemplos de expressões

A tabela a seguir fornece algumas expressões de exemplo e descrições de suas interpretações pelo analisador de linguagem de consulta. 

| Expression                     | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IFD/XMP/EXIF: autor            | Corresponde ao seguinte caminho de navegação: IFD Block-> XMP Block-> Propriedade "Author" no esquema "EXIF".                                                                                                                                                                                                                                            |
| /\[1 \] IFD/ \[ 0 \] XMP/EXIF: autor | O mesmo que o primeiro item nessa tabela, exceto que o \[ \# \] prefixo descreve qual item deve ser navegado em caso de uma colisão de nomes.                                                                                                                                                                                                                                |
| /IFD/{UShort = 700}/Author       | O mesmo que o primeiro item nesta tabela, exceto que ele usa uma expressão de dados para referenciar o bloco XMP em vez do nome do bloco "XMP" (o bloco XMP é incorporado sob o identificador curto de marca curta não assinado 700). Além disso, a propriedade "autor" não especifica um esquema. O analisador de consulta tentará corresponder a propriedade em todos os esquemas e retornará a primeira correspondência. |
| /ifd/xmp                       | Fornece um caminho de navegação para um bloco de metadados. Se o bloco for encontrado, um novo leitor/gravador de metadados será retornado.                                                                                                                                                                                                                                                 |
| /\[\*\]Texto/palavra-chave            | Obtém ou define a propriedade de palavra-chave para uma parte do PNG. Como a especificação de metadados png permite várias partes de um tipo específico, a \[ \* \] notação Obtém/define a parte do png de dados com a propriedade apropriada. De acordo com a especificação do PNG, duas partes não podem ter as mesmas propriedades.                                                                |



 

Cada bloco de metadados também é identificado exclusivamente pelo GUID de metadados que pode ser usado no lugar do nome de bloco amigável. A sintaxe a seguir pode ser usada no lugar de fornecer nomes de bloco: "/{GUID = GUID}/ \[ n \] {GUID = GUID}/Schema: tagidentifier"

A tabela a seguir fornece alguns exemplos inválidos e os motivos pelos quais eles seriam rejeitados. 

| Expressão inválida         | Descrição da rejeição                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /IFD/ \[ 0 \] \[ 2 \] EXIF/       | Rejeitado porque não há suporte para índices de matriz multidimensionais.                                                                                                    |
| /IFD/{UShort = 1}/{UShort = 2} | Rejeitado a menos que IFD tenha um tagID = 1, que é um manipulador de metadados que contém um item de metadados com um tagID = 2.                                                        |
| /{ushort = 1}                | Rejeitado se o processamento da consulta for relativo a um nível superior da hierarquia de metadados. Isso ocorre porque o nível superior contém apenas blocos de metadados e não itens de dados. |



 

## <a name="photo-metadata-policy-expressions"></a>Expressões de política de metadados de foto

Conforme observado anteriormente, uma expressão de consulta totalmente qualificada começa com uma barra (/). As expressões que não começam com a barra são avaliadas como expressões de política. uma expressão de política permite consultar os metadados de foto para [propriedades do Shell](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)Windows relacionadas à imagem. Na seção seleção de dados anteriormente neste documento, a expressão "/XMP/XMP: rating" foi usada para acessar a propriedade de classificação XMP. Essa propriedade também pode ser consultada usando a seguinte expressão de política:

-   System. SimpleRating

Para acessar a propriedade de classificação do esquema MicrosoftPhoto, a seguinte expressão de consulta pode ser usada:

-   System. rating

As expressões de política de metadados de foto se comportam de forma diferente das consultas de metadados totalmente qualificadas de maneiras notáveis.

Primeiro, ao acessar metadados usando uma expressão de política, o WIC executa a arbitragem e a resolução de conflitos, caso a mesma propriedade esteja disponível em vários blocos de metadados. Por exemplo, os valores de classificação MicrosoftPhoto e XMP são armazenados no bloco App1/IFD e no bloco XMP. A política de metadados de foto determina a precedência para qual valor de bloco é retornado ao ler metadados. Quando você estiver gravando metadados, a política de metadados de foto garantirá que as mesmas propriedades em diferentes blocos sejam consistentes. Se você usar uma consulta de metadados como "/XMP/XMP: rating", será responsável por arbitrar entre os vários locais de metadados.

> [!Note]  
> Para obter uma lista das expressões de política com suporte e suas políticas de mapeamento, consulte o tópico [políticas de metadados de fotos](photo-metadata-policies.md) .

 

Segundo, as expressões de política de metadados de foto são independentes do formato de imagem, enquanto as consultas de metadados totalmente qualificadas não são. Por exemplo, a consulta "/XMP/XMP: rating" é específica para o formato JPEG. As imagens TIFF também dão suporte a metadados XMP, mas são armazenadas de forma diferente em relação ao JPEG, portanto, a consulta TIFF seria "/IFD/XMP/XMP: rating". No entanto, em ambos os casos, a expressão de política seria "System. SimpleRating".

As expressões de política de metadados de foto fornecem um nível mais alto de abstração e simplicidade quando comparadas a consultas de metadados totalmente qualificadas e, portanto, devem ser preferidas em casos onde o acesso de metadados de nível baixo não é necessário. No entanto, as expressões de política fornecem acesso apenas a um conjunto limitado de metadados de imagem, enquanto a linguagem de consulta de metadados fornece acesso a quase todos os metadados armazenados em um arquivo de imagem.

## <a name="metadata-query-language-summary"></a>Resumo da linguagem de consulta de metadados

A tabela a seguir é uma definição formal da linguagem de consulta de metadados do WIC. Cada símbolo de gramática representa uma expressão composta por outros símbolos. A expressão pode ser outro símbolo ou uma sequência de outros símbolos separados pela barra vertical ( \| ), indicando uma opção "ou". A expressão inteira à direita é uma possível substituição para o símbolo especificado à esquerda. 

| Símbolo                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item>\| <indexed item>&lt; index&gt;                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | ' < ' \<name> ' > '                                                                                                                                                    |
| \<item>             | \<name>\| \& lt; &gt; \<data> índice \|\<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \&lt; índice&gt;            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | "char" \| "UCHAR" \| "short" \| "UShort" \| "Long" \| "ULONG" " \| int" \| "UINT" \| "LONGLONG" \| "ULONGLONG" \| "Float" \| "Double" \| "Str" " \| WSTR" "GUID" " \| \| bool" |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | número                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da leitura e da escrita de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Como codificar uma imagem JPEG com metadados](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



