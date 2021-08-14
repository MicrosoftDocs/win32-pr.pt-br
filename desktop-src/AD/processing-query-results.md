---
title: Processando os resultados da pesquisa
description: Após a primeira chamada para IDirectorySearch GetFirstRow ou IDirectorySearch GetNextRow, S \_ OK, S \_ ADS \_ NOMORE ROWS ou um resultado de erro \_ é retornado.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Ing Search Results AD
- Active Directory, pesquisando, processando resultados da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185200"
---
# <a name="processing-the-search-results"></a>Processando os resultados da pesquisa

Após a primeira chamada para [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch::GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), **S \_ OK,** **S ADS \_ \_ NOMORE \_ ROWS** ou um resultado de erro é retornado.

Se o valor de retorno **for S \_ ADS \_ NOMORE \_ ROWS,** nenhum outro objeto correspondente ao filtro foi encontrado. Se um resultado de erro for retornado, a consulta falhará. Em ambos os casos, você não precisa processar as linhas no resultado porque nada foi retornado.

Se **S \_ OK** for retornado, uma linha será recuperada. Você pode analisar as colunas por nome usando [**IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). O nome é **lDAPDisplayName** do atributo na coluna. O conjunto de todas as colunas foi definido pelo parâmetro pAttributeNames do [**método IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) Se **NULL** tiver sido especificado, o conjunto de todas as colunas será a união de todas as propriedades encontradas para todos os objetos retornados. Para ler todo o conjunto de colunas retornadas para um objeto, use [**iDirectorySearch::GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) para iterar cada coluna e use o nome da coluna retornado para chamar **IDirectorySearch::GetColumn**.

O [**método IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) retorna uma estrutura [**ADS SEARCH \_ \_ COLUMN**](/windows/desktop/api/iads/ns-iads-ads_search_column) que contém o nome do atributo, o tipo do atributo, a contagem de valores e um ponteiro para uma matriz de estruturas [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que contêm os valores. Você pode fazer um loop pelas **estruturas ADSVALUE** para ler os valores da propriedade retornada pela coluna. Você deve ler o membro apropriado da estrutura **ADSVALUE** com base no [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) especificado pelo membro **dwADsType** da estrutura **ADS SEARCH \_ \_ COLUMN** (ou o **membro dwType** da estrutura **ADSVALUE).** Por exemplo, se **dwADsType** fosse **ADSTYPE \_ INTEGER,** você leria o membro **Inteiro** de cada **estrutura ADSVALUE.**

Para obter mais informações e um exemplo de código, consulte [Código de exemplo para pesquisar usuários.](example-code-for-searching-for-users.md)

 

 