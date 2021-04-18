---
description: Para desenhar um retângulo sombreado, defina uma matriz de trivértices com dois elementos e uma única estrutura de retângulo de GRADIENTe \_ . O exemplo de código a seguir mostra como desenhar um retângulo sombreado usando a função GradientFill com o modo de preenchimento de GRADIENTe \_ \_ definido.
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: Desenhando um retângulo sombreado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502425"
---
# <a name="drawing-a-shaded-rectangle"></a>Desenhando um retângulo sombreado

Para desenhar um retângulo sombreado, defina uma matriz de [**TRIvértices**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) com dois elementos e uma única estrutura de [**\_ retângulo de gradiente**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) . O exemplo de código a seguir mostra como desenhar um retângulo sombreado usando a função [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) com o modo de preenchimento de gradiente \_ \_ definido.


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



A imagem a seguir mostra a saída de desenho do exemplo de código anterior.

![ilustração mostrando um retângulo com um preenchimento gradual de escuro no lado esquerdo para acender no lado direito](images/gradientfillrectangle.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de bitmaps](bitmaps.md)
</dt> <dt>

[Funções de bitmap](bitmap-functions.md)
</dt> <dt>

[Desenhando um triângulo sombreado](drawing-a-shaded-triangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**retângulo de GRADIENTe \_**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**Trivértice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



