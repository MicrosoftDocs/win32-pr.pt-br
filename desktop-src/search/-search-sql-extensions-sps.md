---
description: O Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Extensões do SQL no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501468"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>Extensões do SQL no Microsoft Windows Search

O Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento. Os aprimoramentos da pesquisa do Windows incluem o seguinte:

## <a name="128-character-identifier-names"></a>128-nomes de identificador de caracteres

Enquanto SQL-92 e SQL-99 restringem colunas e outros identificadores para 18 caracteres, o Windows Search dá suporte a nomes de coluna de 128 caracteres. Para obter mais informações, consulte [Identificadores](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Agrupando resultados por colunas

As consultas podem especificar como agrupar os resultados. Você pode especificar os intervalos pelos quais agrupar e pode especificar mais de uma coluna para Agrupamento. Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e pode aninhar agrupamentos. Para obter mais informações, consulte [agrupar em... SOBRE... Instrução](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Pesquisa de Diacritic-Insensitive

Além de Pesquisar que não diferencia maiúsculas de minúsculas, a pesquisa do Windows dá suporte à pesquisa que não é sensível a diacríticos (sinais de acentuação). Para obter mais informações, consulte [sensibilidade de diacríticos em pesquisas](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Peso da coluna

As consultas que pesquisam mais de uma coluna podem especificar a importância de cada coluna. Os predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) dão suporte à ponderação de coluna.

## <a name="null-predicate"></a>Predicado nulo

Embora a indexação de conteúdo de texto completo não tenha nenhum conjunto definido de colunas, as consultas podem exigir que os membros do conjunto de resultados tenham ou não colunas especificadas. Não é possível diferenciar entre um documento tem uma propriedade especificada com o valor definido como **NULL** e um documento que não tem a propriedade.

## <a name="rank-modification"></a>Modificação de classificação

Você pode manipular a classificação de resultados da pesquisa usando [pesos](-search-sql-understandingrelevancevalues.md) em Propriedades e em grupos de propriedades com alias. A coerção de classificação dá suporte à manipulação direta da classificação de relevância com base nos critérios especificados.

 

 



