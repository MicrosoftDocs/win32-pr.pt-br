---
description: 'Um padrão de hachura é feito de duas cores: um para o plano de fundo e outro para as linhas que formam o padrão em segundo plano.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Preenchendo uma forma com um padrão de hachura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987873"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Preenchendo uma forma com um padrão de hachura

Um padrão de hachura é feito de duas cores: um para o plano de fundo e outro para as linhas que formam o padrão em segundo plano. Para preencher uma forma fechada com um padrão de hachura, use um objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) . O exemplo a seguir demonstra como preencher uma elipse com um padrão de hachura:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



A ilustração a seguir mostra a elipse preenchida.

![ilustração de uma elipse preenchida com um padrão de hachura de linhas horizontais em um plano de fundo sólido](images/hatch1.png)

O construtor [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) usa três argumentos: o estilo de hachura, a cor da linha de hachura e a cor do plano de fundo. O argumento de estilo de hachura pode ser qualquer elemento da enumeração [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) . Há mais de 50 elementos na enumeração **HatchStyle** ; alguns desses elementos são mostrados na lista a seguir:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



