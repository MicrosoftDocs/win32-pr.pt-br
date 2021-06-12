---
description: Saiba mais sobre o argumento SUBQUERY Windows Search. Uma subconsistência é um arquivo de pesquisa salvo que você pode usar como um filtro para uma nova consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento SUBQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011029"
---
# <a name="subquery-argument-windows-search"></a>Argumento SUBQUERY (Windows Search)

Uma subconsistência é um arquivo de pesquisa salvo ( .search-ms) que você pode usar como um \* filtro para uma nova consulta. Os resultados da subconsistência são usados como a origem da nova consulta. Por exemplo, digamos que você tenha vários arquivos de pesquisa salvos que restringem uma consulta por lista de distribuição por email: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. O uso `subquery` do argumento permite limitar as pesquisas de email a qualquer ou todas essas pesquisas salvas.

Este tópico é organizado da seguinte forma:

-   [Exemplo](#example)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com Parameter-Value argumentos](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos do identificador de localidade](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento DESaRELAÇÃO](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



