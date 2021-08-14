---
description: As dimensões de uma caneta geométrica são especificadas em unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Canetas geométricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 748efb1748634b4fd5add35b62a7e6e8c576293f20eee62421674f59128821f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699238"
---
# <a name="geometric-pens"></a>Canetas geométricas

As dimensões de uma caneta geométrica são especificadas em unidades lógicas. Portanto, as linhas desenhadas com uma caneta geométrica podem ser dimensionadas, ou seja, elas podem parecer mais largas ou mais estreitas, dependendo da transformação do mundo atual. Para obter mais informações sobre a transformação mundial, consulte [Espaços e transformações de coordenadas.](coordinate-spaces-and-transformations.md)

Além dos três atributos compartilhados com canetas cosméticas (largura, estilo e cor), as canetas geométricas têm os quatro atributos a seguir: padrão, hatch opcional, estilo final e estilo de junção. Para obter mais informações sobre esses atributos, consulte [Atributos de caneta.](pen-attributes.md)

Para criar uma caneta geométrica, um aplicativo usa a [**função ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Assim como com canetas cosméticas, a [**função SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleciona uma caneta geométrica no DC do aplicativo.

 

 



