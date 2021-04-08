---
description: Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento de subconsulta (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920766"
---
# <a name="subquery-argument-windows-search"></a>Argumento de subconsulta (pesquisa do Windows)

Uma subconsulta é um arquivo de pesquisa salvo ( \* . Search-MS) que você pode usar como um filtro para uma nova consulta. Os resultados da subconsulta são usados como a origem para a nova consulta. Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição de email: myDepartment. Search-MS, teamproject. Search-MS e corporatewide. Search-MS. O uso do `subquery` argumento permite que você limite as pesquisas de email a qualquer ou a todas essas pesquisas salvas.

Este tópico é organizado da seguinte maneira:

-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos do identificador de localidade](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento de trilha](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento de sintaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



