---
description: Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função. Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função AngleArc.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Linhas e curvas combinadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967696"
---
# <a name="combined-lines-and-curves"></a>Linhas e curvas combinadas

Além de desenhar linhas ou curvas, os aplicativos podem desenhar combinações de saída de linha e de curva chamando uma única função. Por exemplo, um aplicativo pode desenhar o contorno de um gráfico de pizza chamando a função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) .

A função [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) desenha um arco ao longo do perímetro de um círculo e desenha uma linha conectando o ponto inicial do arco ao centro do círculo. Além de usar a função **AngleArc** , um aplicativo também pode combinar a saída de linha e de curva irregular usando a função do [**polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) .

 

 



