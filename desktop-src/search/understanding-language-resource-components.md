---
description: Os recursos de idioma consistem em separadores de palavras e lematizadores que estendem os recursos de criação e consulta de índice para novas linguagens e localidades.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Noções básicas sobre componentes de recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8feb10d14edbf4aba59b912ae1945d5e87ec32ef684f0b1f5530f1770ba70053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462378"
---
# <a name="understanding-language-resource-components"></a>Noções básicas sobre componentes de recursos de idioma

Os recursos de idioma consistem em separadores de palavras e lematizadores que estendem os recursos de criação e consulta de índice para novas linguagens e localidades. Os separadores de palavras são usados durante a criação e consulta de índice. Os lematizadores são usados somente para consulta. Windows A pesquisa usa DLLs de recurso de idioma para associar a implementações [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para uma localidade de idioma específica.

Este tópico é organizado da seguinte maneira:

-   [Sobre os recursos de idioma](#about-language-resources)
-   [Quebra de palavras](#word-breaking)
-   [Lematização](#stemming)
-   [Normalização](#normalization)
-   [Palavras de ruído](#noise-words)
-   [Tópicos relacionados](#related-topics)

## <a name="about-language-resources"></a>Sobre os recursos de idioma

Windows A pesquisa usa um filtro (uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) e [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para acessar um documento em seu formato nativo. O componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) extrai o conteúdo do texto, as propriedades e a formatação do documento. O [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica a localidade do documento que está filtrando. O componente de indexação invoca o separador de palavras apropriado para essa localidade. Se nenhum estiver disponível, o componente de indexação invocará o separador de palavras neutro. O separador de palavras recebe, de um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), um fluxo de entrada de caracteres Unicode que o separador de palavras analisa para produzir palavras e frases individuais. O separador de palavras também normaliza os formatos de data e hora. O indexador normaliza as palavras produzidas pelo separador de palavras convertendo as palavras para todas as letras maiúsculas. O indexador salva as palavras em maiúsculas no índice de texto completo, com exceção das palavras de ruído identificadas para essa localidade.

a tabela a seguir lista as ações e os resultados correspondentes da frase "a figura 1 ilustra a função dos recursos de idioma para Windows pesquisa durante o processo de criação de índice."



| Ação                  | Texto resultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Texto original           | a figura 1 ilustra a função de recursos de idioma para Windows pesquisa durante o processo de criação de índice.                    |
| Filtragem               | a figura 1 ilustra a função de recursos de idioma para Windows pesquisa durante o processo de criação de índice.                    |
| Quebra de palavras           | figura, 1, ilustra,, função, de, idioma, recursos, para, Windows, pesquisar, durante, o, índice, criação, processo, EOS |
| Normalização           | FIGURA, 1, ILUSTRA,, FUNÇÃO, DE, IDIOMA, RECURSOS, WINDOWS, PESQUISA, DURANTE, O, ÍNDICE, CRIAÇÃO, PROCESSO           |
| Remoção de palavras de ruído      | FIGURA, ILUSTRAÇÕES, FUNÇÃO, IDIOMA, RECURSOS, WINDOWS, PESQUISAR, DURANTE, ÍNDICE, CRIAÇÃO, PROCESSO                            |
| Salvar no índice de texto completo | FIGURA, ILUSTRAÇÕES, FUNÇÃO, IDIOMA, RECURSOS, WINDOWS, PESQUISAR, DURANTE, ÍNDICE, CRIAÇÃO, PROCESSO                            |



 

Separadores de palavras e lematizadores são usados para expandir consultas [FREETEXT](-search-sql-freetext.md) no momento da consulta. A localidade da consulta é a localidade padrão, a menos que um LCID (identificador de código de idioma) seja passado como um parâmetro de consulta. O componente de consulta invoca o separador de palavras apropriado nos termos da consulta listados na cláusula [Where](-search-sql-where.md) da consulta. Por exemplo, se a cláusula WHERE da consulta contiver "FREETEXT (maçãs, laranjas e pêras)", o separador de palavras receberá o texto "maçãs, laranjas e pêras". Se a cláusula WHERE da consulta usar o predicado [Contains](-search-sql-contains.md) de texto completo, a saída de texto do separador de palavras será normalizada. Caso contrário, o componente de consulta passa cada palavra identificada pelo separador de palavras para o lematizador apropriado para esse idioma e localidade. O lematizador gera uma lista de formulários alternativos, ou formas flexionadas, para essa palavra. O componente de consulta normaliza a lista expandida de termos de consulta e remove palavras de ruído.

A tabela a seguir lista as ações e os resultados correspondentes da consulta "maçãs, laranjas e pêras".



| Ação                       | Texto resultante                                            |
|------------------------------|-----------------------------------------------------------|
| Texto original                | maçãs, laranjas e pêras                                |
| Quebra de palavras                | maçãs, laranjas, e pêras, EOS                          |
| Lematização                     | Apple, maçãs, laranja, laranjay, laranjas e pêras, pêras |
| Normalização                | APPLE, MAÇÃS, LARANJA, LARANJAY, LARANJAS E PÊRAS, PÊRAS |
| Remoção de palavras de ruído           | APPLE, MAÇÃS, LARANJA, LARANJAY, LARANJAS, PÊRA, PÊRAS      |
| Lista expandida de termos de consulta | APPLE, MAÇÃS, LARANJA, LARANJAY, LARANJAS, PÊRA, PÊRAS      |



 

Os termos de consulta expandidos aumentam a probabilidade de que a consulta Localize documentos que correspondam à intenção da consulta original. O texto que o separador de palavras ou o lematizador gera no momento da consulta não é armazenado no disco.

## <a name="word-breaking"></a>Quebra de palavras

A quebra de palavras é a separação do texto em tokens de texto individuais ou palavras. Muitas linguagens, especialmente aquelas com alfabetos romanos, têm uma matriz de separadores de palavras (como espaços em branco) e pontuação que são usadas para discernir palavras, frases e frases. Os separadores de palavras devem contar com a heurística de linguagem precisa para fornecer resultados confiáveis e precisos. A quebra de palavras é mais complexa para sistemas baseados em caracteres de escrita ou alfabetos baseados em script, em que o significado de caracteres individuais é determinado do contexto. Para obter mais informações sobre considerações linguísticas que podem afetar a implementação do seu separador de palavras, consulte [considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Lematização

Windows A pesquisa aplica os lematizadores exclusivamente no momento da consulta para gerar formas de palavras adicionais para os termos nas consultas [FREETEXT](-search-sql-freetext.md) e Property. Os lematizadores executam a análise de morfológicas e aplicam regras gramaticais para gerar uma lista de formulários alternativos, ou formas flexionadas, para palavras. Formulários alternativos geralmente têm a mesma haste ou formulário base. Ao gerar os formulários formas flexionadas para uma palavra, o serviço de indexação retorna os resultados da consulta que são estatisticamente mais relevantes para uma consulta. Por exemplo, uma consulta de texto completo para "refinar correspondência" corresponde a documentos que contêm "nada, nada mais, nada mais, nada mais, Swam, swum" ou "reunião, encontro, atende, atende a", reunião, cumprido "e combinações desses termos.

Alguns idiomas exigem que os termos de formas flexionadas sejam gerados no momento do índice e no tempo de consulta para inflexões padrão e variante. Nesse caso, a lematização acontece no componente de separador de palavras, com o mínimo de trabalho de lematização no lematizador real. Por exemplo, o separador de palavras em Japonês executa a lematização durante a criação do índice e consulta para habilitar uma consulta para localizar diferentes formas formas flexionadas dos termos de pesquisa.

## <a name="normalization"></a>Normalização

Os documentos de todos os idiomas são armazenados em um único índice. Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são manipuladas consistentemente em todos os separadores de palavras. Para obter mais informações sobre as considerações de normalização que podem afetar a implementação do seu separador de palavras, consulte [normalização do formulário de superfície](surface-form-normalization.md).

## <a name="noise-words"></a>Palavras de ruído

Palavras de ruído, também conhecidas como palavras de parada, são palavras que não são indicadores significativos para o conteúdo. O serviço de indexação remove palavras de ruído dos termos de consulta e do conteúdo incluído no índice de texto completo. Um *deslocamento* é a ocorrência de uma palavra em um documento ou em uma lista de termos de consulta. O deslocamento das palavras de ruído em um documento ou consulta é registrado como em branco. A remoção de palavras de ruído melhora o desempenho da consulta, evitando o crescimento desnecessário do índice. Ele também melhora a relevância dos resultados da consulta. você pode configurar Windows pesquisa para usar listas de palavras de ruído para idiomas específicos. Essas listas são usadas quando um separador de palavras é invocado para esse idioma. Por exemplo, "o" no idioma inglês ocorre com tanta frequência que tem pouco valor como uma chave exclusiva. "O" está na lista de palavras de ruído, não é gravado no índice de conteúdo e, se consultado, não retorna nenhum resultado.

As palavras de ruído atuam como espaços reservados em consultas de frase. Um documento que contém o texto "Wag The Dog" é armazenado no índice com "Wag" na ocorrência 1 e "Dog" na ocorrência 3. A consulta de frase "Wag Dog" não corresponde, mas a consulta de frase "Wag a Dog" faz, porque a informação de ocorrência corresponde. A frase "Wag roxo Dog" não corresponde porque "roxo" não foi encontrado no índice na ocorrência 2. No entanto, uma consulta para "Wag The Dog" retorna documentos que contêm "Wag roxo Dog" porque não há como determinar com eficiência se o documento tinha uma palavra que não é de ruído entre "Wag" e "Dog".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estendendo recursos de linguagem](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Implementando um disjuntor de palavras e um stemmer](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considerações linguísticas e Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Solução de problemas de recursos de linguagem e práticas recomendadas](troubleshooting-language-resources.md)
</dt> </dl>

 

 
