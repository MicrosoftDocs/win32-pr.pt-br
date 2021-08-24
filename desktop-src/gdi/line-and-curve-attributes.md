---
description: Um DC (contexto de dispositivo) contém atributos que afetam a saída de linha e de curva. Os atributos line e Curve incluem a posição atual, o estilo do pincel, a cor do pincel, o estilo da caneta, a cor da caneta, a transformação e assim por diante.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Atributos de linha e de curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5ab8758cf6e77b28568cacafd8c57312c052d9e9415211f034e3d1a70b6c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831606"
---
# <a name="line-and-curve-attributes"></a>Atributos de linha e de curva

Um DC (contexto de dispositivo) contém atributos que afetam a saída de linha e de curva. Os *atributos line e Curve* incluem a posição atual, o estilo do pincel, a cor do pincel, o estilo da caneta, a cor da caneta, a transformação e assim por diante.

A posição atual padrão de qualquer DC está localizada no ponto (0, 0) em espaço lógico (ou mundial). Você pode definir essas coordenadas para uma nova posição chamando a função [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e passando um novo conjunto de coordenadas.

> [!Note]  
> Há dois conjuntos de funções de desenho de linha e de curva. O primeiro conjunto retém a posição atual em um controlador de domínio e o segundo conjunto altera a posição. Você pode identificar as funções que alteram a posição atual examinando o nome da função. Se o nome da função terminar com a preposição "to", a função definirá a posição atual como o ponto final da última linha desenhada ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**Polilineto**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)ou [**polibezierto**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Se o nome da função não terminar com essa preposição, ele deixará a posição atual intacta ([**arco**](/windows/desktop/api/Wingdi/nf-wingdi-arc), [**polilinha**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)ou [**polibezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

O pincel padrão é um pincel branco sólido. Um aplicativo pode criar um novo pincel chamando a função [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) . Depois de criar um pincel, o aplicativo pode selecioná-lo em seu controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows fornece um conjunto completo de funções para criar, selecionar e alterar o pincel no DC de um aplicativo. Para obter mais informações sobre essas funções e sobre pincéis em geral, consulte [pincéis](brushes.md).

A caneta padrão é uma caneta preta superficial e sólida que tem um pixel de largura. Um aplicativo pode criar uma caneta usando a função [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Depois de criar uma caneta, seu aplicativo pode selecioná-la em seu controlador de domínio chamando a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows fornece um conjunto completo de funções para criar, selecionar e alterar a caneta no DC de um aplicativo. Para obter mais informações sobre essas funções e sobre as canetas em geral, consulte [canetas](pens.md).

A transformação padrão é a transformação do Unity (especificada pela matriz de identidade). Um aplicativo pode especificar uma nova transformação chamando a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) . Windows fornece um conjunto completo de funções para transformar linhas e curvas alterando sua largura, localização e aparência geral. Para obter mais informações sobre essas funções, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).

 

 



