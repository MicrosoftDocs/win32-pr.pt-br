---
description: As dimensões de uma caneta geométrica são especificadas em unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Canetas geométricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988812"
---
# <a name="geometric-pens"></a>Canetas geométricas

As dimensões de uma caneta geométrica são especificadas em unidades lógicas. Portanto, as linhas desenhadas com uma caneta geométrica podem ser escaladas ou seja, elas podem parecer mais largas ou estreitas, dependendo da transformação do mundo atual. Para obter mais informações sobre a transformação do mundo, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).

Além dos três atributos compartilhados com canetas superficiais (largura, estilo e cor), as canetas geométricas possuem os quatro atributos a seguir: padrão, hachura opcional, estilo final e estilo de junção. Para obter mais informações sobre esses atributos, consulte [atributos de caneta](pen-attributes.md).

Para criar uma caneta geométrica, um aplicativo usa a função [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Assim como nas canetas superficiais, a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleciona uma caneta geométrica no controlador de domínio do aplicativo.

 

 



