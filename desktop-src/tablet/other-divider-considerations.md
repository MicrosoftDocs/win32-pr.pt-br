---
description: 'Considere o seguinte ao decidir quando e como usar o objeto Divisor em um aplicativo:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Outras considerações sobre divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3328fd553a16aeee1e1dfa5459b78a45732a55494e0481950d730dab7ce0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449356"
---
# <a name="other-divider-considerations"></a>Outras considerações sobre divisor

Considere o seguinte ao decidir quando e como usar o [**objeto Divisor**](inkdivider-class.md) em um aplicativo:

-   O [**objeto Divisor**](inkdivider-class.md) foi projetado para separar desenhos e blocos de manuscrito, mas não para reconhecer níveis mais altos de estrutura, como tabelas ou colunas.
-   O [**objeto Divisor**](inkdivider-class.md) não fornece interfaces especificamente para correção dos resultados da análise de layout.
-   O uso do tempoout e do número de heurísticas de traço para adicionar ou remover vários traços por vez dos traços no objeto [**Divisor**](inkdivider-class.md) pode melhorar o desempenho.

## <a name="reanalysis-considerations"></a>Considerações sobre reanálise

Se você estiver considerando usar o objeto [**Divisor**](inkdivider-class.md) em um aplicativo em que o objeto **Divisor** pode ter que reanalizar grandes quantidades de tinta, lembre-se do seguinte.

### <a name="retaining-copies-of-ink-and-strokes"></a>Retendo cópias de tinta e traços

Um aplicativo pode manter cópias de [**objetos Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) para elementos de aplicativo que podem ser revisitados posteriormente na sessão do aplicativo. Isso elimina a necessidade de reanalizar o **objeto Ink** se o usuário retornar ao elemento . Essa abordagem troca memória para melhorar o desempenho.

### <a name="data-reduction-heuristics"></a>Heurística de redução de dados

Você pode ser capaz de registrar os resultados da análise como dados do aplicativo e implementar a heurística para determinar quando reanalizar um conjunto de traços. Essa prática reduziria a necessidade de reanalizar toda a tinta no aplicativo entre as sessões do aplicativo. No entanto, é necessário ter cuidado para preservar os limites do elemento estrutural ou para reanalizar todos os traços dos elementos afetados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe InkDivider**](inkdivider-class.md)
</dt> <dt>

[Classe Microsoft.Ink.Divider](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
