---
description: Este tópico descreve as considerações de lematização para idiomas agglutinative e pares de substitutos Unicode, e para usar pares substitutos para estender o conjunto de caracteres Unicode para acomodar diferentes conjuntos de caracteres.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Considerações lingüísticas e Unicode diversas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433fb212917f29acbc2347c3324668a77533dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010382"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Considerações lingüísticas e Unicode diversas

Este tópico descreve as considerações de lematização para idiomas agglutinative e pares de substitutos Unicode, e para usar pares substitutos para estender o conjunto de caracteres Unicode para acomodar diferentes conjuntos de caracteres. Este tópico também descreve como os separadores de palavras identificam frases no texto e manipulam espaços não separáveis e como separadores de palavras e lematizadores lidam com números e datas, palavras compostas, frases compostas, palavras especiais e caracteres, acrônimos e abreviações e capitalização.

Este tópico é organizado da seguinte maneira:

-   [Identificação da frase](#phrase-identification)
-   [Idiomas agglutinative](#agglutinative-languages)
-   [Números, horas e datas](#numbers-times-and-dates)
-   [Palavras compostas](#compound-words)
-   [Frases compostas](#compound-phrases)
-   [Caracteres especiais e palavras](#special-characters-and-words)
-   [Acrônimos e abreviações](#acronyms-and-abbreviations)
-   [Uso de maiúsculas](#capitalization)
-   [Espaços não separáveis](#nonbreaking-spaces)
-   [Pares substitutos](#surrogate-pairs)

## <a name="phrase-identification"></a>Identificação da frase

Frases são uma palavra ou um grupo de palavras que são modificadas por uma ou mais outras. Frases são difíceis de identificar consistentemente porque o mesmo modificador pode ser usado em mais de uma frase com o mesmo substantivo. Por exemplo, "nova casa", "casa de Parliament", "nova casa de Parliament."

O Windows Search usa frases com mais frequência no momento da consulta. As frases no texto da consulta recebem um peso maior do que palavras individuais. No exemplo anterior, um documento contendo "House de Parliament" é classificado como maior que um contendo "House" e "Parliament" em pontos diferentes no documento. Recomendamos que os separadores de palavras gerem uma frase no momento da consulta se for provável que a frase corresponda a pelo menos um documento.

## <a name="agglutinative-languages"></a>Idiomas agglutinative

As linguagens agglutinative formam palavras por meio da combinação de morphemes menores para expressar ideias compostas. Cada um desses morphemes geralmente tem um significado ou função e mantém seu formulário original e significa durante o processo de combinação. Para idiomas que têm agglutinative morphology, como turco, finlandês, húngaro ou coreano, é possível produzir milhares de formulários para uma determinada palavra raiz.

A tabela a seguir mostra uma lista de formas flexionadas Forms para a palavra finlandesa "talo" ("House").



| Word      | Tradução   |
|-----------|---------------|
| Talo      | Doméstica         |
| Taloni    | Minha casa      |
| Talossa   | Na casa  |
| Talossani | Em minha casa   |
| Taloja    | Abriga        |
| Taloissa  | Nos casas |



 

As linguagens formas flexionadas, como Inglês, francês e latim, têm um número muito pequeno de formas de palavras possíveis para uma palavra raiz. Em linguagens formas flexionadas, morphemes influenciam uma na outra durante a associação. A maioria das alterações na inflexão está presente no final ou na palavra que termina. Em contraste com os idiomas agglutinative, as linguagens formas flexionadas tendem a ter diferentes funções para um único morpheme. Por exemplo, um morpheme pode determinar tanto o número quanto o caso.

Os lematizadores para os idiomas agglutinative devem avaliar a compensação entre o desempenho e a precisão para gerar apenas um subconjunto do número de formas de palavras possíveis.

## <a name="numbers-times-and-dates"></a>Números, horas e datas

Os separadores de palavras devem usar um formato comum para representar números, horários e datas para facilitar consultas consistentes.

Quando você cria um separador de palavras, recomendamos que o separador de palavras Normalize números a uma representação canônica usando o padrão "NN *DD* D *CC*", em que nn é a sequência literal "nn", *DD* é a parte inteira do número, D é o literal "d" e *CC* é a parte fracionária do número. Os separadores de palavras não restringem o número de dígitos para o inteiro ou para a parte fracionária do número. Recomendamos que os separadores de palavras reconheçam padrões numéricos que são delimitados por ambos os pontos (.) e vírgulas (,). Por exemplo, o Windows Search representa "1000,2" e "1.000, 2" como "NN1000D2".

Escolha um formato para o separador de palavras e lematizador. Numerais árabes de byte único são normalizados de forma que uma consulta que contenha qualquer um desses formulários corresponda a documentos com outros formulários.

Quando você cria um separador de palavras, recomendamos que o separador de palavras apresente todas as horas como uma representação de 24 horas usando o padrão "TT *HHMMSS*", onde TT é o prefixo literal "tt", *hh* é a hora, *mm* é o minutos e *SS* é os segundos. O Windows Search não corresponde a unidades de tempo adicionais, como milissegundos. Análise da manhã e P.M. padrões é opcional.

Quando você cria um separador de palavras, recomendamos que o separador de palavras gere datas no formato canônico de "DD *aaaammdd*", em que DD é o literal "dd", *yyyy* é o ano, *mm* é o mês e *DD* é o dia. Também recomendamos que os separadores de palavras armazenem anos com dois dígitos nos formatos de vinte e vigésimo-primeiro século. Por exemplo, separadores de palavras representam "2.2.99" como "DD19990202" e "DD20990202". No momento da consulta, a pesquisa do Windows deriva a data usando as APIs (interfaces de programação de aplicativo) do Windows para determinar a data de cruzamento do servidor para exibir o formato correto, 19 *XX* ou 20 *XX*.

## <a name="compound-words"></a>Palavras compostas

Em alguns idiomas, como o alemão, os substantivos são compostos de substantivos mais simples. Esses substantivos compostos são muito específicos no sentido de um cancelamento de consulta razoável. Por exemplo, sem decomposição, uma consulta para "Versicherung" ("seguro") não corresponde a "Lebensversicherungsgesellschaft" ("vendas de seguros da vida útil"). Em casos como esse, recomendamos que os separadores de palavras quebrem essas palavras compostas em componentes básicos durante a criação do índice e o tempo de consulta. O separador de palavras em alemão quebra "Lebensversicherungsgesellschaft" nas palavras do componente "Leben", "Versicherung" e "Gesellschaft". Ele aplica a mesma decomposição no momento da consulta, juntamente com a lematização opcional para cada um dos termos resultantes.

## <a name="compound-phrases"></a>Frases compostas

Alguns idiomas, como o coreano, contêm frases complexas que podem ser quebradas de várias maneiras diferentes. Uma frase coreana consiste em *palavras de conteúdo*, como substantivos, prosubstantivos, verbos e adjetivos, seguidos por *palavras funcionais*. As palavras funcionais são encontradas em post-posições e terminações. Post-posições indicam a função funcional do substantivo ou pronoun em uma sentença; terminações indicam a função funcional do verbo ou do adjetivo.

Uma frase pode ter várias análises, e cada análise pode consistir em várias palavras de conteúdo. O separador de palavras deve empregar heurística específica a um idioma para determinar, do contexto, quanto peso fornecer a análises diferentes. O separador de palavras pode determinar qual decomposição usar com base no número de palavras de componentes resultantes. Alguns separadores de palavras podem favorecer pequenas seqüências de termos mais longos, enquanto outros separadores de palavras podem favorecer seqüências longas de palavras menores.

Outra consideração é que, em coreano, os substantivos e os subsubstantivos podem ser armazenados no índice sem suas palavras funcionais correspondentes. O coreano é uma linguagem agglutinative e combina várias terminações de palavra com verbos e adjetivos para formar inúmeros formulários de formas flexionadas. Verbos e adjetivos identificados em frases são salvos com suas terminações no índice, mas o separador de palavras não gera novos formulários.

## <a name="special-characters-and-words"></a>Caracteres especiais e palavras

Caracteres especiais são caracteres como "," "©" e "™". Esses caracteres raramente são usados em consultas. Os separadores de palavras devem remover caracteres especiais durante a criação do índice e no momento da consulta.

Recomendamos que os separadores de palavras reconheçam palavras especiais, como "C++", "C", " \# .net," notas e notação musical. Os separadores de palavras podem usar uma heurística de idioma para identificar um padrão para palavras especiais. Os separadores de palavras também podem usar um dicionário personalizado que contenha palavras especiais reconhecidas.

## <a name="acronyms-and-abbreviations"></a>Acrônimos e abreviações

Os acrônimos e as abreviações devem ser considerados quando você implementa um separador de palavras. Em muitos idiomas, as letras individuais de acrônimos são separadas por pontos. Ocasionalmente, palavras que não são acrônimos ou abreviações reconhecidas são abreviadas. Por exemplo, "Estados Unidos da América" pode ser abreviado como "EUA" ou "EUA" Os separadores de palavras incluídos no Windows Search geralmente identificam palavras de uma única letra como palavras de ruído e tratam essas palavras como espaços reservados durante o tempo de consulta. Durante o tempo de consulta, um separador de palavras que não reconhece acrônimos comuns ou que não reconheça abreviações, converte a abreviação "Estados Unidos" em "U", "S" e "A". Essa decomposição não fornece informações suficientes para corresponder palavras no índice de texto completo, pois todos os termos de consulta são palavras de ruído. Quando você cria um separador de palavras, recomendamos que o separador de palavras remova os períodos que separam as cartas de acrônimos. No exemplo, "Estados Unidos" é armazenado como "EUA" e um termo de consulta que contém "EUA" na verdade, consulta para "EUA". Se um separador de palavras processar uma abreviação, o período nessa abreviação não será tratado como um intervalo de EOS. Por isso, um separador de palavras pode não identificar corretamente uma interrupção de EOS se a abreviação estiver no final da sentença.

## <a name="capitalization"></a>Uso de maiúsculas

No momento, o Windows Search não preserva a capitalização quando salva palavras no índice de texto completo. Separadores de palavras e lematizadores não devem modificar o caso de palavras.

## <a name="nonbreaking-spaces"></a>Espaços não separáveis

Quando você cria um separador de palavras, recomendamos que você verifique se o separador de palavras trata espaços não separáveis como separadores de palavras. Também é recomendável que o separador de palavras gere formas alternativas da palavra, com e sem espaços não separáveis. Alguns caracteres, como sublinhados, são caracteres especiais tratados como caracteres não separáveis devido às fontes do texto no qual eles são encontrados. Por exemplo, o código-fonte ou nomes de arquivo podem incluir sublinhados como caracteres não separáveis.

## <a name="surrogate-pairs"></a>Pares substitutos

Pares substitutos são representações de caractere no código-fonte que representam um único caractere que consiste em uma sequência de dois valores Unicode. Em um par codificado, o primeiro valor é um substituto alto e o segundo é um substituto baixo. Um substituto alto é um caractere no intervalo de U + D800 até U + DBFF. Um substituto baixo é um caractere no intervalo de U + DC00 até U + DFFF. Os pares substitutos estendem o conjunto de caracteres além do caractere Unicode. É recomendável que um separador de palavras use as seguintes regras ao lidar com pares substitutos:

-   Um substituto alto deve preceder um substituto baixo.
-   Um substituto baixo deve seguir um substituto alto.
-   Um substituto alto ou baixo sem um valor correspondente para sua outra metade não tem significado.

Os separadores de palavras devem considerar quaisquer pares e gerar os pares como tal no índice. Para obter mais informações, consulte [substitutos e caracteres suplementares](/windows/desktop/Intl/surrogates-and-supplementary-characters).

 

 
