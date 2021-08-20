---
description: a linguagem de consulta do Microsoft Windows search dá suporte a seis predicados de pesquisa de texto não completo. Os predicados descritos nesta seção estão listados na tabela a seguir.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Predicados de texto não completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915120106e98fd031571b1b974bb09957c9fa02790c050e81374e7717b269d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680507"
---
# <a name="non-full-text-predicates"></a>Predicados de texto não completo

a linguagem de consulta do Microsoft Windows search dá suporte a seis predicados de pesquisa de texto não completo. Os predicados descritos nesta seção estão listados na tabela a seguir.



| Predicado de texto não completo                                                    | Descrição                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Todos os bits e a bit a bit](all-bitwise.md)                            | É um conjunto de palavras-chave que estão prestes a testar os bits em um tipo integral.                                                                                                               |
| [Função DATEADD](-search-sql-dateadd.md)                                | Executa cálculos de data e hora para propriedades correspondentes com tipos de data. Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.     |
| [Predicado LIKE](-search-sql-like.md)                                     | Compara valores de coluna usando a correspondência de padrão simples com caracteres curinga.                                                                                                          |
| [Comparação de valor literal](-search-sql-literalvaluecomparison.md)         | Compara valores de coluna com valores literais de cadeia de caracteres, data, carimbo de hora, numéricos e outros. Esse predicado dá suporte a desigualdades, como maior que (' > ') e menor que (' < '). |
| [Comparações de vários valores (matriz)](-search-sql-multivaluedcomparisons.md) | Compara colunas com valores de multivalors em uma matriz de valores literais.                                                                                                                   |
| [Predicado nulo](-search-sql-null.md)                                     | Detecta valores de coluna indefinidos para o documento.                                                                                                                              |



 

> [!IMPORTANT]
> as consultas de pesquisa que usam o predicado **NULL** podem exigir que Windows pesquisa verifique todo o catálogo, o que pode retardar o desempenho da consulta.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



