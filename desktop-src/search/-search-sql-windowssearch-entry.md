---
description: O Windows Search fornece recursos de rastreamento e pesquisa de conteúdo que dão suporte à pesquisa de texto completo. A linguagem de consulta usada pelo Windows Search estende a sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Consultando o índice com a sintaxe SQL do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460982"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Consultando o índice com a sintaxe SQL do Windows Search

O Windows Search fornece recursos de rastreamento e pesquisa de conteúdo que dão suporte à pesquisa de texto completo. A linguagem de consulta usada pelo Windows Search estende a sintaxe de consulta de banco de dados SQL-92 e SQL-99 padrão para aprimorar sua utilidade com pesquisas baseadas em texto.

Todos os recursos do Windows Search linguagem SQL (SQL) são compatíveis com o Windows Search no Windows Vista e posterior, incluindo todas as versões do Windows 10.

Esta seção fornece uma visão geral da sintaxe SQL no Windows Search e inclui os seguintes tópicos:

- [Visão geral da sintaxe SQL do Windows Search](-search-sql-ovwofsearchquery.md)
- [Informações gerais da linguagem de consulta](-search-sql-generalqueryinfo.md)
- [AGRUPAR EM... SOBRE... Privacidade](-search-sql-group-on-over.md)
- [Instrução SELECT](-search-sql-select.md)
- [Cláusula FROM](-search-sql-from.md)
- [Cláusula WHERE](-search-sql-where.md)
- [Cláusula ORDER BY](-search-sql-orderby.md)
- [CLASSIFICAR por cláusula](-search-sql-rankby.md)
- [Instrução SET](-search-sql-set.md)
- [Propriedades do conjunto de linhas](-search-sql-rowset-properties.md)

Esta documentação pressupõe familiaridade com a vinculação de objetos e o banco de dados de incorporação (OLE DB) e SQL.

## <a name="code-samples"></a>Exemplos de código

O exemplo de código WSSQL demonstra como se comunicar entre o Microsoft OLE DB e o Windows Search por meio do SQL. O exemplo de código WSOleDB ilustra Active Template Library (ATL) OLE DB acesso aos aplicativos do Windows Search e dois métodos adicionais para recuperar os resultados do Windows Search. Ambos os exemplos estão disponíveis nos [exemplos do Windows Search](-search-samples-ovw.md) e no [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Tópicos relacionados

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)

[Usando abordagens SQL e AQS para consultar o índice](-search-3x-wds-qryidx-overview.md)

[Consultando o índice com ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Consultando o índice com o protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)

[Consultando o índice com a sintaxe SQL do Windows Search](-search-sql-windowssearch-entry.md)

[Usando a sintaxe de consulta avançada programaticamente](-search-3x-advancedquerysyntax.md)
