---
description: O sombreamento suave é um método de sombreamento de uma região com um gradiente de cor.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Sombreamento suave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170534"
---
# <a name="smooth-shading"></a>Sombreamento suave

O *sombreamento suave* é um método de sombreamento de uma região com um gradiente de cor. Incluir informações de cor, junto com os limites de desenho primitivo, especifica o gradiente de cor. A GDI interpola linearmente a cor do interior do primitivo passado nos pontos de extremidade de cor. As informações de cor e vértice estão incluídas nas informações de posição na estrutura de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .

Use a função [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) para preencher uma estrutura de triângulo ou de retângulo. Para preencher um triângulo com sombreamento suave, chame **GradientFill** com os três pontos de extremidade do triângulo. Para preencher um retângulo com sombreamento suave, chame **GradientFill** com as coordenadas de retângulo superior esquerda e inferior direita. **GradientFill** faz referência às estruturas [**trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**\_ retângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)e [**\_ triângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .

Para obter um exemplo, consulte [desenhando um triângulo sombreado](drawing-a-shaded-triangle.md).

 

 



