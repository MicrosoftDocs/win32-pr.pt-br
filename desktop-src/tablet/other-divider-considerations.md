---
description: 'Considere o seguinte ao decidir quando e como usar o objeto divisória em um aplicativo:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Outras considerações sobre divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170462"
---
# <a name="other-divider-considerations"></a>Outras considerações sobre divisor

Considere o seguinte ao decidir quando e como usar o objeto [**divisória**](inkdivider-class.md) em um aplicativo:

-   O objeto [**divisória**](inkdivider-class.md) é projetado para separar desenhos e blocos de manuscrito, mas não para reconhecer níveis mais altos de estrutura, como tabelas ou colunas.
-   O objeto [**divisória**](inkdivider-class.md) não fornece interfaces especificamente para a correção de resultados da análise de layout.
-   O uso do tempo limite e do número de heurística de traço para adicionar ou remover vários traços por vez dos traços no objeto de [**divisória**](inkdivider-class.md) pode melhorar o desempenho.

## <a name="reanalysis-considerations"></a>Considerações de reanálise

Se você estiver considerando o uso do objeto [**divisor**](inkdivider-class.md) em um aplicativo em que o objeto **divisor** pode ter que reanalisar grandes quantidades de tinta, tenha em mente o seguinte.

### <a name="retaining-copies-of-ink-and-strokes"></a>Retenção de cópias de tinta e traços

Um aplicativo pode manter cópias de objetos [**Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) para elementos de aplicativo que podem ser revisitados posteriormente na sessão do aplicativo. Isso elimina a necessidade de reanalisar o objeto de **tinta** se o usuário retornar ao elemento. Essa abordagem compensa a memória para melhorar o desempenho.

### <a name="data-reduction-heuristics"></a>Heurística de redução de dados

Você pode registrar os resultados da análise como dados do aplicativo e implementar a heurística para determinar quando reanalisar um conjunto de traços. Essa prática reduziria a necessidade de analisar novamente toda a tinta no aplicativo entre as sessões do aplicativo. No entanto, deve-se ter cuidado para preservar os limites de elementos estruturais ou para reanalisar todos os traços dos elementos afetados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe InkDivider**](inkdivider-class.md)
</dt> <dt>

[Classe Microsoft. Ink. divisor](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
