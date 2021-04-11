---
description: O protocolo Search-MS? Application é uma Convenção para consultar o índice do Windows Search.
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: Introdução com argumentos de Parameter-Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164332"
---
# <a name="getting-started-with-parameter-value-arguments"></a>Introdução com argumentos de Parameter-Value

A **pesquisa-MS** ? o [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) é uma Convenção para consultar o índice do Windows Search. O protocolo permite que aplicativos, como o Windows Explorer, consultem o índice com argumentos de valor de parâmetro, incluindo argumentos de propriedade, pesquisas salvas anteriormente, sintaxe de consulta avançada (AQS), sintaxe de consulta natural (NQS) e identificadores de código de idioma (LCIDs) para o indexador e a própria consulta.

Este tópico é organizado da seguinte maneira:

- [Sobre argumentos de Parameter-Value](#about-parameter-value-arguments)
- [Exemplos](#examples)
- [Tópicos relacionados](#related-topics)

## <a name="about-parameter-value-arguments"></a>Sobre argumentos de Parameter-Value

O protocolo Search-MS usa a seguinte sintaxe codificada por URL padrão:

```
search-ms:parameter=value[&parameter=value]&
```

A sintaxe começa identificando o próprio protocolo (Search-MS:). Os pares parâmetro/valor são argumentos passados para o mecanismo de pesquisa, conforme descrito na tabela a seguir.

| Parâmetro                                                    | Valor                                                         | Descrição                                                                                                                                                                                                                                                                | Versão                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Consulta                                                        | Texto codificado por URL                                              | O texto da consulta inserido pelo usuário.                                                                                                                                                                                                                                        | Windows XP e posterior    |
| [InputLocale](-search-3x-wds-qryidx-localeidentifiers.md)   | Qualquer LCID válido                                                | O LCID que identifica o idioma de entrada para a consulta.                                                                                                                                                                                                                 | Windows XP e posterior    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | Qualquer LCID válido                                                | O LCID que identifica o idioma da versão internacional do indexador. O padrão é 1033 (en-US).                                                                                                                                                            | Windows XP e posterior    |
| [estrutural](-search-3x-wds-qryidx-crumb.md)                     | Instrução AQS                                                 | Esse argumento restringe o escopo que está sendo pesquisado. No Windows Vista e posterior, o Search-MS dá suporte a AQS completas, bem como a uma implementação especial para um `location` argumento. No Windows XP, o Search-MS também dá suporte a AQS completas, exceto para uma implementação especial do `kind` e do `store` . | Windows XP e posterior    |
| [sintaxe](-search-3x-wds-qryidx-syntaxargument.md)           | NQS, AQS (não diferencia maiúsculas de minúsculas)                                 | A sintaxe de consulta a ser usada para pesquisar o índice: sintaxe de consulta natural ou sintaxe de consulta avançada (AQS). AQS é o padrão e sempre é presumido, analisado e suportado.                                                                                                    | Windows Vista e posterior |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | Qualquer propriedade válida do sistema de propriedades                   | Uma propriedade que especifica a coluna pela qual os resultados são empilhados.                                                                                                                                                                                                                  | Windows Vista e posterior |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | Um caminho totalmente especificado para um arquivo de pesquisa salvo ( \* . Search-MS) | Os resultados da subconsulta são usados como a origem da consulta. Ou seja, os termos de consulta são pesquisados em relação aos resultados da subconsulta.                                                                                                                           | Windows Vista e posterior |
| displayname                                                  | Cadeia de caracteres codificada em URL                                            | O nome da pesquisa atual.                                                                                                                                                                                                                                            | Windows Vista e posterior |


Para obter informações relacionadas, consulte [registrando um aplicativo em um protocolo de URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)).

## <a name="examples"></a>Exemplos

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>Tópicos relacionados

[Argumentos do identificador de localidade](-search-3x-wds-qryidx-localeidentifiers.md)

[Argumento de trilha](-search-3x-wds-qryidx-crumb.md)

[Argumento de sintaxe](-search-3x-wds-qryidx-syntaxargument.md)

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
