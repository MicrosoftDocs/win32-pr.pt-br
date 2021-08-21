---
description: Os recursos de linguagem consistem em disjuntores de palavras e stemmers que estendem os recursos de criação e consulta de índice para novas linguagens e localidades.
ms.assetid: 7963805e-e279-42cf-ba95-f81a7de8e68e
title: Noções básicas sobre componentes de recursos de linguagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8feb10d14edbf4aba59b912ae1945d5e87ec32ef684f0b1f5530f1770ba70053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462378"
---
# <a name="understanding-language-resource-components"></a>Noções básicas sobre componentes de recursos de linguagem

Os recursos de linguagem consistem em disjuntores de palavras e stemmers que estendem os recursos de criação e consulta de índice para novas linguagens e localidades. Os disjuntores de palavras são usados durante a criação e a consulta do índice. Os stemmers são usados apenas para consulta. Windows A pesquisa usa DLLs de recurso de linguagem para se vincular a [**implementações IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para uma localidade de idioma específica.

Este tópico é organizado da seguinte forma:

-   [Sobre recursos de linguagem](#about-language-resources)
-   [Quebra de palavras](#word-breaking)
-   [Lematização](#stemming)
-   [Normalização](#normalization)
-   [Palavras de ruído](#noise-words)
-   [Tópicos relacionados](#related-topics)

## <a name="about-language-resources"></a>Sobre recursos de linguagem

Windows A pesquisa usa um filtro (uma implementação da interface [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) e [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para acessar um documento em seu formato nativo. O [**componente IFilter**](/windows/win32/api/filter/nn-filter-ifilter) extrai conteúdo de texto, propriedades e formatação do documento. O [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) identifica a localidade do documento que está filtrando. O componente de indexação invoca o disjuntor de palavras apropriado para essa localidade. Se nenhum estiver disponível, o componente de indexação invocará o disjuntor de palavras neutro. O disjuntor de palavras recebe, de [**um IFilter,**](/windows/win32/api/filter/nn-filter-ifilter)um fluxo de entrada de caracteres Unicode analisados pelo disjuntor de palavras para produzir palavras e frases individuais. O disjuntor de palavras também normaliza formatos de data e hora. O indexador normaliza as palavras produzidas pelo disjuntor de palavras convertendo as palavras em todas as letras maiúsculas. O indexador salva as palavras maiúsculas no índice de texto completo, com exceção das palavras de ruído identificadas para essa localidade.

A tabela a seguir lista as ações e os resultados correspondentes para a frase "A Figura 1 ilustra a função dos recursos de linguagem para Windows Search durante o processo de criação do índice".



| Ação                  | Texto resultante                                                                                                               |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Texto original           | A Figura 1 ilustra a função dos recursos de linguagem para Windows Search durante o processo de criação do índice.                    |
| Filtragem               | A Figura 1 ilustra a função dos recursos de linguagem para Windows Search durante o processo de criação do índice.                    |
| Quebra de palavras           | Figura, 1, ilustra, a função, de, idioma, recursos, para, Windows, Pesquisar, durante, o índice, a criação, o processo, o EOS |
| Normalização           | FIGURA, 1, ILUSTRA, A FUNÇÃO, DE, IDIOMA, RECURSOS, WINDOWS, PESQUISA, DURANTE, O, ÍNDICE, CRIAÇÃO, PROCESSO           |
| Remoção de palavras de ruído      | FIGURA, ILUSTRA, FUNÇÃO, IDIOMA, RECURSOS, WINDOWS, PESQUISA, DURANTE, ÍNDICE, CRIAÇÃO, PROCESSO                            |
| Salvar no índice de texto completo | FIGURA, ILUSTRA, FUNÇÃO, IDIOMA, RECURSOS, WINDOWS, PESQUISA, DURANTE, ÍNDICE, CRIAÇÃO, PROCESSO                            |



 

Os disjuntores de palavras e os stemmers são usados para expandir [consultas FREETEXT](-search-sql-freetext.md) no momento da consulta. A localidade da consulta é a localidade padrão, a menos que um LCID (identificador de código de idioma) seja passado como um parâmetro de consulta. O componente de consulta invoca o disjuntor de palavras apropriado nos termos de consulta listados na [cláusula WHERE](-search-sql-where.md) da consulta. Por exemplo, se a cláusula WHERE da consulta contiver "FREETEXT (maçãs, laranjas e peras)," o disjuntor de palavras receberá o texto , "maçãs, laranjas e peras". Se a cláusula WHERE de consulta usar o predicado [CONTAINS](-search-sql-contains.md) de texto completo, a saída de texto do disjuntor de palavras será normalizada. Caso contrário, o componente de consulta passa cada palavra identificada pelo disjuntor de palavras para o stemmer apropriado para esse idioma e localidade. O stemmer gera uma lista de formulários alternativos ou inflectados para essa palavra. O componente de consulta normaliza a lista expandida de termos de consulta e remove palavras de ruído.

A tabela a seguir lista as ações e os resultados correspondentes para a consulta "maçãs, laranjas e peras".



| Ação                       | Texto resultante                                            |
|------------------------------|-----------------------------------------------------------|
| Texto original                | maçãs, laranjas e peras                                |
| Quebra de palavras                | maçãs, laranjas e, peras, EOS                          |
| Lematização                     | apple, apples, orange, orangey, oranges e, pear, pears |
| Normalização                | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, AND, PEAR, PEARS |
| Remoção de palavras de ruído           | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |
| Lista expandida de termos de consulta | APPLE, APPLES, ORANGE, ORANGEY, ORANGES, PEAR, PEARS      |



 

Os termos de consulta expandidos aumentam a probabilidade de que a consulta encontre documentos que corresponderem à intenção da consulta original. O texto que o quebra-texto ou o stemmer gera no momento da consulta não é armazenado em disco.

## <a name="word-breaking"></a>Quebra de palavras

Quebra de palavras é a separação de texto em tokens de texto individuais ou palavras. Muitas linguagens, especialmente aquelas com alfabetos latinos, têm uma matriz de separadores de palavras (como espaço em branco) e pontuação que são usadas para distinguir palavras, frases e frases. Os disjuntores de palavras devem contar com heurística de linguagem precisa para fornecer resultados confiáveis e precisos. A quebra de palavras é mais complexa para sistemas baseados em caracteres de escrita ou alfabetos baseados em script, em que o significado dos caracteres individuais é determinado do contexto. Para obter mais informações sobre considerações linguísticas que podem afetar sua implementação de disjuntor de palavras, consulte [Considerações linguísticas e Unicode](linguistic-and-unicode-considerations.md).

## <a name="stemming"></a>Lematização

Windows A pesquisa aplica-se a stemmers exclusivamente no momento da consulta para gerar formulários de palavras adicionais para termos em [FREETEXT](-search-sql-freetext.md) e consultas de propriedade. Os stemmers executam análise morfológica e aplicam regras gramaticais para gerar uma lista de formulários alternativos ou inflectados para palavras. Formulários alternativos geralmente têm o mesmo formato de caução ou base. Ao gerar os formulários inflectados para uma palavra, o Serviço de Indexação retorna resultados de consulta que são estatisticamente mais relevantes para uma consulta. Por exemplo, uma consulta de texto completo para "reunião de nadação" corresponde a documentos que contêm "nadando, nadando, nadando, nadando", nadando, nadando, nadando, swum" ou "meet, meet's, meet, meets', meeting, met" e combinações desses termos.

Alguns idiomas exigem que termos inflectados sejam gerados no tempo de índice e no tempo de consulta para inflecções padrão e variantes. Nesse caso, a derivação ocorre no componente de disjuntor de palavras, com trabalho de derivação mínimo no stemmer real. Por exemplo, o disjuntor de palavras japonês executa a derivação durante a criação e a consulta de índice para permitir que uma consulta encontre diferentes formas inflectadas dos termos de pesquisa.

## <a name="normalization"></a>Normalização

Documentos de todos os idiomas são armazenados em um único índice. Embora as palavras e as regras linguísticas sejam significativamente diferentes, há algumas considerações, como números, datas e horas, que são tratadas de forma consistente em todos os disjuntores de palavras. Para obter mais informações sobre considerações de normalização que podem afetar sua implementação de disjuntor de palavras, consulte [Normalização do Surface Form](surface-form-normalization.md).

## <a name="noise-words"></a>Palavras de ruído

Palavras de ruído, também conhecidas como palavras de parada, são palavras que não são indicadores significativos para o conteúdo. O Serviço de Indexação remove palavras de ruído dos termos de consulta e do conteúdo incluído no índice de texto completo. Um *deslocamento* é a ocorrência de uma palavra em um documento ou em uma lista de termos de consulta. O deslocamento de palavras de ruído em um documento ou consulta é registrado como em branco. A remoção de palavras de ruído melhora o desempenho da consulta, evitando o crescimento desnecessário do índice. Ele também melhora a relevância dos resultados da consulta. Você pode configurar o Windows Search para usar listas de palavras de ruído para idiomas específicos. Essas listas são usadas quando um disjuntor de palavras é invocado para esse idioma. Por exemplo, "o" no idioma inglês ocorre com tanta frequência que tem pouco valor como uma chave exclusiva. "O" está na lista de palavras de ruído, não é gravado no índice de conteúdo e, se consultado, não retorna nenhum resultado.

Palavras de ruído atuam como espaço reservados em consultas de frase. Um documento que contém o texto "nome do cachorro" é armazenado no índice com "cachorro" na ocorrência 1 e "cachorro" na ocorrência 3. A consulta de frase "cachorro de cachorro" não corresponde, mas a consulta de frase "um cachorro" corresponde, porque as informações de ocorrência coincidem. A frase "cachorro roxo de roxo" não é encontrada porque "roxo" não é encontrado no índice na ocorrência 2. No entanto, uma consulta para "nomear o cachorro" retorna documentos que contêm "cachorro roxo", pois não há nenhuma maneira de determinar com eficiência se o documento tinha uma palavra sem ruído entre "cachorro" e "cachorro".

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

 

 
