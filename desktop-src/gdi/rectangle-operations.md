---
description: A função SetRect cria um retângulo, a função CopyRect faz uma cópia de um determinado retângulo, e a função SetRectEmpty cria um retângulo vazio.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operações de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296577"
---
# <a name="rectangle-operations"></a>Operações de retângulo

A função [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) cria um retângulo, a função [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) faz uma cópia de um determinado retângulo, e a função [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) cria um retângulo vazio. Um retângulo vazio é qualquer retângulo com largura zero, altura zero ou ambos. A função [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se um determinado retângulo está vazio. A função [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se dois retângulos são idênticos ou seja, se eles têm as mesmas coordenadas.

A função [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta ou diminui a largura ou altura de um retângulo, ou ambos. Ele pode adicionar ou remover largura de ambas as extremidades do retângulo; Ele pode adicionar ou remover altura das partes superior e inferior do retângulo.

A função [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) move um retângulo por um determinado valor. Ele move o retângulo adicionando o valor x, o valor y ou os valores x e y determinados às coordenadas de canto.

A função [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se um determinado ponto está dentro de um determinado retângulo. O ponto estará no retângulo se ele estiver no lado esquerdo ou superior ou estiver completamente dentro do retângulo. O ponto não estará no retângulo se ele estiver no lado direito ou inferior.

A função [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) cria um novo retângulo que é a interseção de dois retângulos existentes, conforme mostrado na figura a seguir.

![ilustração mostrando dois retângulos sobrepostos, com sombreamento mais escuro para indicar a interseção ](images/csrec-01.png)

A função [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) cria um novo retângulo que é a União de dois retângulos existentes, conforme mostrado na figura a seguir.

![ilustração de dois retângulos sobrepostos, com sombreamento mais escuro indicando áreas dentro da União, mas não dentro de um retângulo](images/csrec-02.png)

Para obter informações sobre as funções que desenham reticências e polígonos, confira [formas preenchidas](filled-shapes.md).

 

 



