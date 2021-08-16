---
description: Você pode desenhar o início ou o fim de uma linha em uma das várias formas chamadas limites de linha. Windows GDI+ dá suporte a várias limites de linha, como arredondado, quadrado, losango e seta.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Desenhando uma linha com limites de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e72e4e1c9c36a7233688378852dfda73196cd7e7131cf7def587ad29a70e82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696156"
---
# <a name="drawing-a-line-with-line-caps"></a>Desenhando uma linha com limites de linha

Você pode desenhar o início ou o fim de uma linha em uma das várias formas chamadas limites de linha. Windows GDI+ dá suporte a várias limites de linha, como arredondado, quadrado, losango e seta.

Você pode especificar limites de linha para o início de uma linha (limite inicial), o final de uma linha (extremidade final) ou os traços de uma linha tracejada (limite de traço).

O exemplo a seguir desenha uma linha com uma ponta de seta em uma extremidade e um limite arredondado na outra extremidade:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



A ilustração a seguir mostra a linha resultante.

![ilustração mostrando uma linha horizontal com uma seta na extremidade esquerda e um círculo na extremidade direita](images/pens4.png)

**LineCapArrowAnchor** e **LineCapRoundAnchor são** elementos da [**enumeração LineCap.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap)

 

 



