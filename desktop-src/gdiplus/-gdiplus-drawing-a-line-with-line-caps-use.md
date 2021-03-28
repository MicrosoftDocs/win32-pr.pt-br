---
description: Você pode desenhar o início ou o final de uma linha em uma das várias formas chamadas line Caps. O Windows GDI+ dá suporte a várias arremates de linha, como round, quadrado, losango e ponta de seta.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Desenhando uma linha com limites de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988244"
---
# <a name="drawing-a-line-with-line-caps"></a>Desenhando uma linha com limites de linha

Você pode desenhar o início ou o final de uma linha em uma das várias formas chamadas line Caps. O Windows GDI+ dá suporte a várias arremates de linha, como round, quadrado, losango e ponta de seta.

Você pode especificar limites de linha para o início de uma linha (Cap inicial), o fim de uma linha (extremidade final) ou os traços de uma linha tracejada (limite de traço).

O exemplo a seguir desenha uma linha com uma ponta de seta em uma extremidade e um limite de arredondamento na outra extremidade:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



A ilustração a seguir mostra a linha resultante.

![ilustração mostrando uma linha horizontal com uma seta na extremidade esquerda e um círculo na extremidade direita](images/pens4.png)

**LineCapArrowAnchor** e **LineCapRoundAnchor** são elementos da enumeração [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .

 

 



