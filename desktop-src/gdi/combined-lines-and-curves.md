---
description: Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função. Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linhas e curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1939b863bfacf2176f15c950b48c8b7c91cc43e7b6b4d4c58ac08e1760c4cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105715"
---
# <a name="combined-lines-and-curves"></a>Linhas e curvas combinadas

Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função. Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

A função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) desenha um arco ao longo do perímetro de um círculo e desenha uma linha conectando o ponto inicial do arco ao centro do círculo. Além de usar a função **AngleArc** , um aplicativo também pode combinar a saída de linha e de curva irregular usando a função do [**polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



