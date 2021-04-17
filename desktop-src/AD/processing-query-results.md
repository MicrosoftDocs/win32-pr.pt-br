---
title: Processando os resultados da pesquisa
description: Após a primeira chamada para IDirectorySearch GetFirstRow ou IDirectorySearch GetNextRow, S \_ OK, s \_ anúncios \_ mais \_ linhas ou um resultado de erro é retornado.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Processando resultados da pesquisa AD
- Active Directory, pesquisando, processando resultados da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732128438162f5ee8f6fe75bb4d2ce53e0d43070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105748297"
---
# <a name="processing-the-search-results"></a>Processando os resultados da pesquisa

Após a primeira chamada para [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), **s \_ OK**, **s anúncios mais \_ \_ \_ linhas** ou um resultado de erro é retornado.

Se o valor de retorno for **S \_ anúncios, \_ mais \_ linhas**, não serão encontrados mais objetos correspondentes ao filtro. Se um resultado de erro for retornado, a consulta falhou. Em ambos os casos, não é necessário processar as linhas no resultado porque nada foi retornado.

Se **S \_ OK** for retornado, uma linha será recuperada. Você pode analisar as colunas por nome usando [**IDirectorySearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). O nome é o **lDAPDisplayName** do atributo na coluna. O conjunto de todas as colunas foi definido pelo parâmetro pAttributeNames do método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) . Se **NULL** tiver sido especificado, o conjunto de todas as colunas será a União de todas as propriedades encontradas para todos os objetos retornados. Para ler todo o conjunto de colunas retornado para um objeto, use o [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) para iterar cada coluna e use o nome da coluna retornado para chamar **IDirectorySearch:: GetColumn**.

O método [**IDirectorySearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) retorna uma estrutura de [**coluna de \_ pesquisa \_ do ADS**](/windows/desktop/api/iads/ns-iads-ads_search_column) que contém o nome do atributo, o tipo do atributo, a contagem de valores e um ponteiro para uma matriz de estruturas [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que contêm os valores. Você pode executar um loop pelas estruturas **ADSVALUE** para ler os valores da propriedade retornada pela coluna. Você deve ler o membro apropriado da estrutura **ADSVALUE** com base no [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) especificado pelo membro **dwADsType** da estrutura de **\_ \_ coluna de pesquisa do ADS** (ou o membro **dwType** da estrutura **ADSVALUE** ). Por exemplo, se **dwADsType** fosse **ADSTYPE \_ inteiro**, você lerá o membro **inteiro** de cada estrutura **ADSVALUE** .

Para obter mais informações e um exemplo de código, consulte [código de exemplo para pesquisa de usuários](example-code-for-searching-for-users.md).

 

 