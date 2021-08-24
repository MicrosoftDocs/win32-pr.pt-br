---
description: Este tópico descreve considerações de derivação para linguagens agregação e pares substitutos Unicode e para usar pares substitutos para estender o conjunto de caracteres Unicode para acomodar conjuntos de caracteres diferentes.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Considerações linguísticas e Unicode diversas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24372194fb17498e1e0ce19be1bbbac3f1dccb27a63d840cedf95de38f735026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594476"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Considerações linguísticas e Unicode diversas

Este tópico descreve considerações de derivação para linguagens agregação e pares substitutos Unicode e para usar pares substitutos para estender o conjunto de caracteres Unicode para acomodar conjuntos de caracteres diferentes. Este tópico também descreve como os disjuntores de palavras identificam frases em texto e lidam com espaços sem quebra e como os disjuntores de palavras e stemmers lidam com números e datas, palavras compostas, frases compostas, palavras e caracteres especiais, abreviações e abreviações e maiúsculas.

Este tópico é organizado da seguinte forma:

-   [Identificação de frase](#phrase-identification)
-   [Linguagens agglutinativas](#agglutinative-languages)
-   [Números, horas e datas](#numbers-times-and-dates)
-   [Palavras compostas](#compound-words)
-   [Frases compostas](#compound-phrases)
-   [Caracteres e palavras especiais](#special-characters-and-words)
-   [Abreviações e acrônimos](#acronyms-and-abbreviations)
-   [Uso de maiúsculas](#capitalization)
-   [Espaços sem abreviação](#nonbreaking-spaces)
-   [Pares substitutos](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificação de frase

Frases são uma palavra ou um grupo de palavras que são modificadas por uma ou mais outras. Frases são difíceis de identificar consistentemente porque o mesmo modificador pode ser usado em mais de uma frase com o mesmo substantivo. Por exemplo, "nova casa", "Casa de Civil", "nova Casa de Civil".

Windows A pesquisa usa frases com mais frequência no momento da consulta. As frases no texto de consulta recebem um peso maior do que as palavras individuais. No exemplo anterior, um documento que contém "Casa de Civil" é classificado como maior do que um que contém "House" e "Civil" em pontos diferentes no documento. Recomendamos que os disjuntores de palavras gerem uma frase no momento da consulta se a frase provavelmente corresponder a pelo menos um documento.

## <a name="agglutinative-languages"></a>Linguagens agglutinativas

Linguagens agglutinativas formam palavras por meio da combinação de morfemos menores para expressar ideias compostas. Cada um desses morphemes geralmente tem um significado ou função e retém sua forma original e significado durante o processo de combinação. Para idiomas que têm amorfologia agglutinativa, como turco, finlandês, húngaro ou coreano, é possível produzir milhares de formulários para uma determinada palavra raiz.

A tabela a seguir mostra uma lista de formulários inflectados para a palavra "talo" em finlandês ("casa").



| Word      | Tradução   |
|-----------|---------------|
| Talo      | Doméstica         |
| Taloni    | Minha casa      |
| Talossa   | Na casa  |
| Talossani | Em minha casa   |
| Taloja    | Casas        |
| Taloissa  | Nas casas |



 

Idiomas inflectados, como inglês, francês e latino, têm um número muito pequeno de formulários de palavras possíveis para uma palavra raiz. Em linguagens inflectadas, os morfemes influenciam um ao outro durante a associação. A maioria das alterações na inflexão está presente no final da palavra ou do tronco. Ao contrário das linguagens agglutinativas, as linguagens inflectadas tendem a ter funções diferentes para um único morpheme. Por exemplo, um morpheme pode determinar o número e o caso.

Os stemmers para linguagens agregação devem avaliar a diferença entre desempenho e precisão para gerar apenas um subconjunto do número de formulários de palavras possíveis.

## <a name="numbers-times-and-dates"></a>Números, horas e datas

Os disjuntores de palavras devem usar um formato comum para representar números, horas e datas para facilitar a consulta consistente.

Quando você cria um disjuntor de palavras, recomendamos que o disjuntor de palavras normalize os números para uma representação canônica usando o padrão "NN *dd* D *cc",* em que NN é a sequência literal "NN", *dd* é a parte inteira do número, D é o literal "D" e *cc* é a parte fracionada do número. Os disjuntores de palavras não restringem o número de dígitos para o inteiro ou a parte da fração do número. Recomendamos que os disjuntores de palavras reconheçam padrões numéricos que são delimitados por períodos (.) e vírgulas (,). Por exemplo, Windows Search representa "1.000.2" e "1.000,2" como "NN1000D2".

Escolha um formato para o disjuntor de palavras e o stemmer. Numerais em árabe de byte único são normalizados de modo que uma consulta que contém qualquer um desses formulários corresponde a documentos com as outras formas.

Quando você cria um disjuntor de palavras, recomendamos que o disjuntor de palavras apresente todas as vezes como uma representação de 24 horas usando o padrão "TT *hhmmss*", em que TT é o prefixo literal "TT", *hh* são as horas, *mm* são os minutos e *ss* são os segundos. Windows A pesquisa não corresponderá a unidades de tempo adicionais, como milissegundos. Análise de A.M. e P.M. os padrões são opcionais.

Quando você cria um disjuntor de palavras, recomendamos que o disjuntor de palavras gere datas no formato canônico de "DD *aaaammmdd",* em que DD é o literal "DD", *aaaaa* são os anos, *mm* são os meses e *dd* são os dias. Também recomendamos que os disjuntores de palavras armazenem anos de dois dígitos em formatos de século e xx e xx primeiro. Por exemplo, os disjuntores de palavras representam "2.2.99" como "DD19990202" e "DD20990202". No momento da consulta, o Windows Search deriva a data usando APIs (interfaces de programação de aplicativos) do Windows para determinar a data de cruzamento para o servidor exibir o formato correto, 19 *XX* ou 20 *XX.*

## <a name="compound-words"></a>Palavras compostas

Em alguns idiomas, como alemão, substantivos são compostos de substantivos mais simples. Esses substantivos compostos são muito específicos em significado para um recall de consulta razoável. Por exemplo, sem decomposição, uma consulta para "Versicherung" ("seguro") não é igual a "Ltdensversicherungsgesellschaft" ("seguro de vida"). Em casos como esse, recomendamos que os disjuntores de palavras quebrem essas palavras compostas em componentes base durante a criação do índice e o tempo de consulta. O disjuntor de palavras alemão interrompe "Arrowensversicherungsgesellschaft" nas palavras de componente "Leben", "Versicherung" e "Gesellschaft". Ele aplica a mesma decomposição no momento da consulta, juntamente com a derivação opcional para cada um dos termos resultantes.

## <a name="compound-phrases"></a>Frases compostas

Algumas linguagens, como o coreano, contêm frases complexas que podem ser interrompidas de várias maneiras diferentes. Uma frase em coreano consiste em palavras de *conteúdo,* como substantivos, pronomes, verbos e adjetivos, seguidos por *palavras funcionais*. Palavras funcionais são encontradas em pós-posições e terminações. Post-positions indicam a função funcional do substantivo ou do pronome em uma frase; terminações indicam a função funcional do verbo ou do adjetivo.

Uma frase pode ter várias análises e cada análise pode consistir em várias palavras de conteúdo. O disjuntor de palavras deve empregar heurística específica do idioma para determinar, do contexto, quanto peso dar a análises diferentes. O disjuntor de palavras pode determinar qual decomposição usar com base no número de palavras de componente resultantes. Alguns disjuntores de palavras podem favorecer sequências curtas de termos mais longos, enquanto outros disjuntores de palavras podem favorecer sequências longas de palavras menores.

Outra consideração é que, em coreano, substantivos e pronomes podem ser os armazenados no índice sem suas palavras funcionais correspondentes. O coreano é uma linguagem agregação e combina várias terminações de palavras com verbos e adjetivos para formar inúmeras formas inflectadas. Verbos e adjetivos identificados em frases são salvos com suas terminações no índice, mas o disjuntor de palavras não gera novos formulários.

## <a name="special-characters-and-words"></a>Caracteres e palavras especiais

Caracteres especiais são caracteres como "," "©" e "™". Esses caracteres raramente são usados em consultas. Os disjuntores de palavras devem retirar caracteres especiais durante a criação do índice e no momento da consulta.

Recomendamos que os disjuntores de palavras reconheçam palavras especiais, como "C++", "C \# ", ".NET", notas e notação de música. Os disjuntores de palavras podem usar uma heurística de linguagem para identificar um padrão para palavras especiais. Os disjuntores de palavras também podem usar um dicionário personalizado que contém palavras especiais reconhecidas.

## <a name="acronyms-and-abbreviations"></a>Abreviações e acrônimos

Acrônimos e abreviações devem ser considerados quando você implementa um disjuntor de palavras. Em muitos idiomas, letras individuais de acrônimos são separadas por pontos. Ocasionalmente, palavras que não são reconhecidas acrônimos ou abreviações são abreviadas. Por exemplo, "Estados Unidos da América" pode ser abreviado como "EUA" ou "EUA". Os disjuntores de palavras incluídos no Windows Search geralmente identificam palavras de letra única como palavras de ruído e tratam essas palavras como espaço reservados durante o tempo de consulta. Durante o tempo de consulta, um disjuntor de palavras que não está ciente de acrônimos comuns ou que não reconhece abreviações converte a abreviação "U.S.A.". em "U", "S" e "A". Essa decomposição não fornece informações suficientes para corresponder palavras no índice de texto completo porque todos os termos de consulta são palavras de ruído. Quando você cria um separador de palavras, recomendamos que o separador de palavras remova os períodos que separam as letras dos acrônimos. No exemplo, "U.S.A.". é armazenado como "EUA" e um termo de consulta que contém "EUA". na verdade, consulta "EUA". Se um disjuntor de palavras processa uma abreviação, o período nessa abreviação não é tratado como uma quebra de EOS. Por isso, um disjuntor de palavras pode não identificar corretamente uma quebra de EOS se a abreviação estiver no final da frase.

## <a name="capitalization"></a>Uso de maiúsculas

Windows No momento, a pesquisa não preserva a capitalização quando salva palavras no índice de texto completo. Os disjuntores de palavras e os stemmers não devem modificar o caso para palavras.

## <a name="nonbreaking-spaces"></a>Espaços sem abreviação

Quando você cria um separador de palavras, recomendamos que você garanta que o separador de palavras trate espaços sem quebra como separadores de palavras. Também é recomendável que o disjuntor de palavras gere formas alternativas da palavra, com e sem espaços sem quebra. Alguns caracteres, como sublinhados, são caracteres especiais que são tratados como caracteres sem abreviação devido às fontes do texto em que são encontrados. Por exemplo, o código-fonte ou os nomes de arquivo podem incluir sublinhados como caracteres não desastados.

## <a name="surrogate-pairs"></a>Pares substitutos

Pares substitutos são representações de caractere no código-fonte que representam um único caractere que consiste em uma sequência de dois valores Unicode. Em um par codificado, o primeiro valor é um substituto alto e o segundo é um substituto baixo. Um substituto alto é um caractere no intervalo U+D800 até U+DBFF. Um substituto baixo é um caractere no intervalo U+DC00 a U+DFFF. Os pares substitutos estendem o conjunto de caracteres além do caractere Unicode. Recomendamos que um disjuntor de palavras use as seguintes regras ao lidar com pares substitutos:

-   Um substituto alto deve preceder um substituto baixo.
-   Um substituto baixo deve seguir um substituto alto.
-   Um substituto alto ou baixo sem um valor correspondente para sua outra metade não tem nenhum significado.

Os disjuntores de palavras devem considerar quaisquer pares e gerar os pares como tal no índice. Para obter mais informações, consulte [Substitutos e caracteres suplementares.](/windows/desktop/Intl/surrogates-and-supplementary-characters)

 

 
