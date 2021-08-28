---
description: A função SetRect cria um retângulo, a função CopyRect faz uma cópia de um determinado retângulo e a função SetRectEmpty cria um retângulo vazio.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operações de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161df56d3534f85cd37701956db0330be59236e3cbbeeed81ef390edd17656bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092756"
---
# <a name="rectangle-operations"></a>Operações de retângulo

A [**função SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) cria um retângulo, a função [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) faz uma cópia de um determinado retângulo e a função [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) cria um retângulo vazio. Um retângulo vazio é qualquer retângulo que tenha largura zero, zero altura ou ambos. A [**função IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se um determinado retângulo está vazio. A [**função EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se dois retângulos são idênticos, ou seja, se eles têm as mesmas coordenadas.

A [**função InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta ou diminui a largura ou a altura de um retângulo ou ambos. Ele pode adicionar ou remover largura de ambas as extremidades do retângulo; ele pode adicionar ou remover a altura da parte superior e inferior do retângulo.

A [**função OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) move um retângulo por uma determinada quantidade. Ele move o retângulo adicionando as quantidades x, y ou x e y determinadas às coordenadas de canto.

A [**função PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se um determinado ponto está dentro de um retângulo determinado. O ponto está no retângulo se ele estiver no lado esquerdo ou superior ou estiver completamente dentro do retângulo. O ponto não está no retângulo se ele estiver no lado direito ou inferior.

A [**função IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) cria um novo retângulo que é a interseção de dois retângulos existentes, conforme mostrado na figura a seguir.

![ilustração mostrando dois retângulos sobrepostos, com sombreamento mais escuro para indicar a interseção ](images/csrec-01.png)

A [**função UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) cria um novo retângulo que é a união de dois retângulos existentes, conforme mostrado na figura a seguir.

![ilustração de dois retângulos sobrepostos, com sombreamento mais escuro indicando áreas dentro da união, mas não dentro de nenhum retângulo](images/csrec-02.png)

Para obter informações sobre funções que desenham relipes e polígonos, consulte [Formas preenchidas.](filled-shapes.md)

 

 



