---
description: o Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL extensões no Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c300b0960e97cba14237bd355e33ae7e42788b1925525e60462d15a5d014e6f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462448"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL extensões no Microsoft Windows Search

o Microsoft Windows Search, com base nos padrões SQL-92 e SQL-99, melhora as pesquisas baseadas em documentos de texto completo em aplicativos de gerenciamento de documentos ou de gerenciamento de conhecimento. Windows As melhorias de pesquisa incluem o seguinte:

## <a name="128-character-identifier-names"></a>128-nomes de identificador de caracteres

embora SQL-92 e SQL-99 restrinjam a coluna e outros identificadores a 18 caracteres, Windows pesquisa oferece suporte a nomes de coluna de 128 caracteres. Para obter mais informações, consulte [Identificadores](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Agrupando resultados por colunas

As consultas podem especificar como agrupar os resultados. Você pode especificar os intervalos pelos quais agrupar e pode especificar mais de uma coluna para Agrupamento. Por exemplo, você pode agrupar os resultados em um intervalo de tamanhos de arquivo (tamanho < 100, 100 <= tamanho < 1000; 1000 <= tamanho) e pode aninhar agrupamentos. Para obter mais informações, consulte [agrupar em... SOBRE... Instrução](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Pesquisa de Diacritic-Insensitive

além de pesquisar que não diferencia maiúsculas de minúsculas, Windows pesquisa dá suporte à pesquisa que não é sensível a diacríticos (sinais de acentuação). Para obter mais informações, consulte [sensibilidade de diacríticos em pesquisas](-search-sql-accentinsensitivitysearches.md).

## <a name="column-weighting"></a>Peso da coluna

As consultas que pesquisam mais de uma coluna podem especificar a importância de cada coluna. Os predicados [Contains](-search-sql-contains.md) e [FREETEXT](-search-sql-freetext.md) dão suporte à ponderação de coluna.

## <a name="null-predicate"></a>Predicado nulo

Embora a indexação de conteúdo de texto completo não tenha nenhum conjunto definido de colunas, as consultas podem exigir que os membros do conjunto de resultados tenham ou não colunas especificadas. Não é possível diferenciar entre um documento tem uma propriedade especificada com o valor definido como **NULL** e um documento que não tem a propriedade.

## <a name="rank-modification"></a>Modificação de classificação

Você pode manipular a classificação de resultados da pesquisa usando [pesos](-search-sql-understandingrelevancevalues.md) em Propriedades e em grupos de propriedades com alias. A coerção de classificação dá suporte à manipulação direta da classificação de relevância com base nos critérios especificados.

 

 



